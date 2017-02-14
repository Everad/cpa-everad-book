# Session
manage your session section. Session data is passed over http cookie, returned to you on calling `login` or `register` endpoints
##Endpoints
{% method %}
####`/session/register`

Register your affiliate account and get session cookie at once
{% sample lang="bash" %}
```bash
curl -X POST -H 'Content-type: application/json' -d '{"email":"test2@example.com", "password":"1"}' -v http://dashboard.everad.com/session/register
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
{% method %}
###`/session/login`
Login to your already registered account
{% sample lang="bash" %}
```bash
curl -X POST -H 'Content-type: application/json' -d '{"email":"test2@example.com", "password":"1"}' -v http://dashboard.everad.com/session/login
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
< Content-Length: 0
```
{% endmethod %}
{% method %}
###`/session/logout`
Logout from your account
{% sample lang="bash" %}
```bash
curl -X POST -v -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' http://dashboard.everad.com/session/logout
```
######success response
```
< HTTP/1.1 200 OK
< Content-Length: 0
```
{% endmethod %}
{% method %}
###`/session/languages`
retrieve available response languages
{% sample lang="bash" %}
```bash
curl -X GET -v -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' http://dashboard.everad.com/session/languages
```
######success response
```
< HTTP/1.1 200 OK
< Content-Type: application/json; charset=utf-8
< Content-Length: 21
["en","ru","ro","th"]
```
{% endmethod %}{% method %}
###`/session/change-language`
change API language to one of `/languages`
{% sample lang="bash" %}
```bash
curl -X POST -v -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' -d '{"language": "ru"}' http://dashboard.everad.com/session/change-language
```
######success response
```
< HTTP/1.1 200 OK
< Content-Type: application/json; charset=utf-8
< Content-Length: 0
["en","ru","ro","th"]
```
{% endmethod %}