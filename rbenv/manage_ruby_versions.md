We <3 [Rbenv](https://github.com/rbenv/rbenv) for managing our Ruby versions on Mac.

To see a list of available Ruby versions for install:
```
$ rbenv install -l
```

Don't see the version you are looking for (aka specified in your gemfile?)?  Then you probably are due for a brew update!
` $ brew update` & ` $ brew upgrade ruby-build`

Check the Ruby versions list again...
```
$ rbenv install -l
```

To install a version:
```
$ rbenv install 2.3.0
```

Before you can bundle and install gems, add bundler:
```
$ gem install bundler
```

Then you can bundle & install all the gems in the gemfile!
```
$ bundle install
```

Wanna get rid of a Ruby version?
```
$ rbenv uninstall 2.3.0-dev
```
