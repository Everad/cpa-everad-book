#Profile
WIP

{% method %}
###`PUT /profile/language`
change API language to one of `/languages`
{% sample lang="bash" %}
```bash
curl -X PUT -v -H 'Content-type: application/json' -d '{"language": "ru"}' -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' http://dashboard.everad.com/v2/profile/language
```
######success response
```
< HTTP/1.1 200 OK
```
######error response
```bash
< HTTP/1.1 400 Bad Request
```
{% endmethod %}