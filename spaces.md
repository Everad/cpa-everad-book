#Spaces
Manage your traffic sources, used in campaigns **TODO specify space types **
##Endpoints
{% method %}
####`GET /spaces`

List your spaces
{% sample lang="bash" %}
```bash
curl -X GET -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' -v http://dashboard.everad.com/v2/spaces
```
######success response
```
< HTTP/1.1 200 OK
[{"id":1,"title":"test space", "type":"social"}]
```
{% endmethod %}
{% method %}
####`POST /spaces`

create new space
{% sample lang="bash" %}
```bash
curl -X POST -d '{"title":"test space", "type":"social"}' -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' -v http://dashboard.everad.com/v2/spaces
```
######success response
```
< HTTP/1.1 201 Created
[{"id":1,"title":"test space", "type":"social"}]
```
{% endmethod %}
{% method %}
####`PUT /spaces/1`

update space
{% sample lang="bash" %}
```bash
curl -X PUT -d '{"title":"test space1", "type":"social"}' -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' -v http://dashboard.everad.com/v2/spaces/1
```
######success response
```
< HTTP/1.1 200 OK
[{"id":1,"title":"test space1", "type":"social"}]
```
{% endmethod %}
{% method %}
####`DELETE /spaces/1`

delete space
{% sample lang="bash" %}
```bash
curl -X DELETE -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' -v http://dashboard.everad.com/v2/spaces/1
```
######success response
```
< HTTP/1.1 200 OK
```
{% endmethod %}





