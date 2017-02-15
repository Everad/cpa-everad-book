#Profile
Manage your profile information
{% method %}
###`GET /profile/balances`
Get account balances
{% sample lang="bash" %}
```bash
curl -X GET -v -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' http://dashboard.everad.com/v2/profile/balances
```
######success response
```
< HTTP/1.1 200 OK
[{
    currency
    balance
    hold
}]
```
{% endmethod %}
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
{% method %}
###`PUT /profile/password`
change your profile password
{% sample lang="bash" %}
```bash
curl -X PUT -v -H 'Content-type: application/json' -d '{"old_password": "1", "new_password":"2"}' -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' http://dashboard.everad.com/v2/profile/password
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
{% method %}
###`GET /profile`
get your profile general info
{% sample lang="bash" %}
```bash
curl -X GET -v -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' http://dashboard.everad.com/v2/profile
```
######success response
```
< HTTP/1.1 200 OK
{
email
skype
phone
manager
status - one of /lists/affiliate-statuses
notificate_news - flag
notificate_tickets - flag
}
```
{% endmethod %}
{% method %}
###`PUT /profile`
update your profile general info
```
phone - can always be updated
skype - can only be updated if previously was empty
notificate_news - flag
notificate_tickets - flag
```
{% sample lang="bash" %}
```bash
curl -X GET -v -H 'Content-type: application/json' -d '{"phone": "11111", "notificate_tickets": true}' -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' http://dashboard.everad.com/v2/profile
```
######success response
```
< HTTP/1.1 200 OK
```
{% endmethod %}



































