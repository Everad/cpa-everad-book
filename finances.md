#Finances
Manage your finances information, payouts
{% method %}
###`GET /finances/payouts`
Get pending payouts
{% endmethod %}
{% method %}
###`POST /finances/payouts`
Create new payout with desired payout system (should be previously connected to your account by `PUT /profile/payout-systems/<id>`

{% sample lang="bash" %}
```bash
curl -v -X POST -H 'Content-type: application/json' -d '{"payout_system_id":1,"amount":9.99}' -b 'connect.sid=s%3AqakdZrNAHauz6JDFBc3j97TN11b4EymV.g7AOMWEFfUatN125nqAnEo0K2th0gYlYX2OKhkUoosw' http://dashboard.everad.com/v2/finances/payouts
```
######success response
```
< HTTP/1.1 200 OK
```
{% endmethod %}


