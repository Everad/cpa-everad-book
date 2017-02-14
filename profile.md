#Profile
WIP

{% method %}
###`/profile/change-language`
change API language to one of `/languages`
{% sample lang="bash" %}
```bash
curl -X POST -v -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' -d '{"language": "ru"}' http://dashboard.everad.com/profile/change-language
```
######success response
```
< HTTP/1.1 200 OK
< Content-Type: application/json; charset=utf-8
< Content-Length: 0
```
######error response
```bash
< HTTP/1.1 400 Bad Request
< Content-Length: 0
```
{% endmethod %}