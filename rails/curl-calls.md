## How to Use cURL to Test Rails controller actions:

##### `-X [action]`:
- Allows you to specify an HTTP action such as GET, POST, PUT or DELETE.

- Example:  
  ```curl -X DELETE 'http://accounting.dev/v1/refunds/1'```


##### `-d [parameter]`:
- Lets you set variables as if they were POSTed in a form to the URL. Note that this automatically makes the request a POST HTTP action type (no -X necessary).

- Example:  
  ```curl -d "refund[amount]=1000" -d "refund[purchase_id]=1234abcd" 'http://accounting.dev/v1/refunds'```


##### `-H [header]`:
- Gives you the option of setting an HTTP header such as Content-Type or Accept. This is particularly useful for requesting text/xml as the Accept type.

- Example:  
  ```curl -H "Accept: text/xml" 'http://accounting.dev/v1/refunds'```


##### `-i, --include`:
- Includes the HTTP-header in the output

- Example:  
  ```curl -i -X PATCH -H "Authorization: Token token=token_id_goes_here" 'http://accounting.dev/v1/refunds/1234abcd'```


---

###### More info on [cURL params](https://curl.haxx.se/docs/manpage.html).
