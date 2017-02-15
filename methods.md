# Session
Session data is passed over http cookie, returned to you on calling `login` or `register` endpoints
##Endpoints
{% method %}
####`POST /session/register`

Register your affiliate account and get session cookie at once
```
email
password
language - one from `/lists/languages`
```
{% sample lang="bash" %}
```bash
curl -X POST -H 'Content-type: application/json' -d '{"email":"test2@example.com", "password":"1", "language":"ru"}' -v http://dashboard.everad.com/v2/session/register
```
######success response
```
< HTTP/1.1 200 OK
< set-cookie: connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0; Path=/; Expires=Fri, 17 Mar 2017 08:49:53 GMT; HttpOnly
```
######error response
```bash
< HTTP/1.1 400 Bad Request
[{"keyword":"uniqueAffiliateEmail","dataPath":".email","schemaPath":"#/properties/email/uniqueAffiliateEmail","params":{"keyword":"uniqueAffiliateEmail"},"message":"should pass \"uniqueAffiliateEmail\" keyword validation"}]
```
{% endmethod %}
{% method %}
###`POST /session/login`
Login to your already registered account
{% sample lang="bash" %}
```bash
curl -X POST -H 'Content-type: application/json' -d '{"email":"test2@example.com", "password":"1"}' -v http://dashboard.everad.com/v2/session/login
```
######success response
```
< HTTP/1.1 200 OK
< set-cookie: connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0; Path=/; Expires=Fri, 17 Mar 2017 08:49:53 GMT; HttpOnly
```
######error response
```bash
< HTTP/1.1 400 Bad Request
```
{% endmethod %}
{% method %}
###`POST /session/logout`
Logout from your account
{% sample lang="bash" %}
```bash
curl -X POST -v -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' http://dashboard.everad.com/v2/session/logout
```
######success response
```
< HTTP/1.1 200 OK
```
{% endmethod %}