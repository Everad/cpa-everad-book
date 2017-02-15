#Spaces
Manage your traffic sources, used in campaigns
##Endpoints
{% method %}
####`/spaces`

Register your affiliate account and get session cookie at once

`email`

`password`

`language` - one from `/lists/languages`
{% sample lang="bash" %}
```bash
curl -X POST -H 'Content-type: application/json' -d '{"email":"test2@example.com", "password":"1", "language":"ru"}' -v http://dashboard.everad.com/v2/session/register
```
######success response
```
< HTTP/1.1 200 OK
< set-cookie: connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0; Path=/; Expires=Fri, 17 Mar 2017 08:49:53 GMT; HttpOnly
< Content-Length: 0
```
######error response
```bash
< HTTP/1.1 400 Bad Request
< Content-Type: application/json; charset=utf-8
< Content-Length: 223
< 
[{"keyword":"uniqueAffiliateEmail","dataPath":".email","schemaPath":"#/properties/email/uniqueAffiliateEmail","params":{"keyword":"uniqueAffiliateEmail"},"message":"should pass \"uniqueAffiliateEmail\" keyword validation"}]
```
{% endmethod %}
