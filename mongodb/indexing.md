# Indexing a collection

- To index a field, do something like this (depending if you want FTS or just to index a field on id):

```
index({ state: 'text' })
index({ instruction_id: 1})
```
> It is VERY important to note that a collection can have AT MOST 1 TEXT INDEX! More [info](https://docs.mongodb.com/manual/core/index-text/#create-text-index).


- Full-text search for entire collection would like something like this:

In the model (eg purchase.rb) file:
```
index({"$**"=>"text"},{name: 'TextIndex'})
```

Then to use in the the controller, (eg purchases_controller.rb) file:
```
Purchase.where({"$text" => {"$search" => search_term}})
```

- To create the indexes in the database: ```$ bin/rake db:mongoid:create_indexes```

- If using compose.io, you can login and, for each collection, view the indexes that have been created on it.  You can remove indexes from the console as well.

- To remove the indexes in the database: ```$ bin/rake db:mongoid:remove_indexes```
