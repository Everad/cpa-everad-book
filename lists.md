#Lists
endpoints for receiving different lists, used by other parts of API
##Endpoints
{% method %}
###`/lists/languages`
retrieve available response languages
{% sample lang="bash" %}
```bash
curl -X GET -v http://dashboard.everad.com/lists/languages
```
######success response
```
< HTTP/1.1 200 OK
< Content-Type: application/json; charset=utf-8
< Content-Length: 21
["en","ru","ro","th"]
```
{% endmethod %}
