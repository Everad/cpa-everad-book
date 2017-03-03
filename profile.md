#Profile
Manage your profile information.
{% method %}
###`GET /profile/balances`
Get account balances. A balance is a wallet for a single currency.
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
###`POST /profile/balances`
Create a new balance for desired currency. Only one currency balance can be created per account.
{% sample lang="bash" %}
```bash
curl -X POST -v -H 'Content-type: application/json' -d '{"currency": "usd"}' -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' http://dashboard.everad.com/v2/profile/balances
```
######success response
```
< HTTP/1.1 200 OK
```
{% endmethod %}

{% method %}
###`PUT /profile/password`
Change your profile password.
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
###`GET /profile/manager`
Get your manager contact info.
{% endmethod %}

{% method %}
###`GET /profile`
Get general info about your profile.
{% sample lang="bash" %}
```bash
curl -X GET -v -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' http://dashboard.everad.com/v2/profile
```
######success response
```
< HTTP/1.1 200 OK
{
language
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
Update your profile general info.
```
language - one of /lists/languages
phone
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
{% method %}
###`GET /profile/payout-systems`
Get available payout systems for your profile balance currencies
{% sample lang="bash" %}
```bash
curl -v -X GET -b 'connect.sid=s%3A8D9teXFlvopv65U1YFayTgBT5iq9WS3R.rhDzTzI4blRSzPwGe6P0PNiZa0otDLMvF4rwsEK4QuU' http://dashboard.everad.com/v2/profile/payout-systems
```
######success response
```
< HTTP/1.1 200 OK
[{"id":1,"title":"рубли наличными","currency":"rub","fields":{"account":{"type":"string"}},"credentials":null}]
```
{% endmethod %}
{% method %}
###`PUT /profile/payout-systems/<id>`
Update payout system's credentials (based on fields from `/profile/payout-systems` request)
{% sample lang="bash" %}
```bash
curl -v -X PUT -H 'Content-type: application/json' -d '{"account": "кошель"}' -b 'connect.sid=s%3A8D9teXFlvopv65U1YFayTgBT5iq9WS3R.rhDzTzI4blRSzPwGe6P0PNiZa0otDLMvF4rwsEK4QuU' http://dashboard.everad.com/v2/profile/payout-systems/1
```
######success response
```
< HTTP/1.1 200 OK
```
{% endmethod %}

{% method %}
###`/profile/novostnik`
{% endmethod %}
{% method %}
###`/profile/global-postback`
{% endmethod %}





































