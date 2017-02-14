# Session

manage your session section. Session data is passed over http cookie, returned to you on calling `login` or `register` endpoints

###Endpoints

{% method %}
`/session/register`

Register your affiliate account and get session cookie at once

{% sample lang="bash" %}

```bash
curl -X POST -H 'Content-type: application/json' -d '{"email":"test2@example.com", "password":"1"}' -v http://dashboard.everad.com/session/register
```
######success response

```
* upload completely sent off: 45 out of 45 bytes
< HTTP/1.1 200 OK
< X-DNS-Prefetch-Control: off
< X-Frame-Options: SAMEORIGIN
< X-Download-Options: noopen
< X-Content-Type-Options: nosniff
< X-XSS-Protection: 1; mode=block
< set-cookie: connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0; Path=/; Expires=Fri, 17 Mar 2017 08:49:53 GMT; HttpOnly
< Date: Tue, 14 Feb 2017 08:49:53 GMT
< Connection: keep-alive
< Content-Length: 0
< 
* Connection #0 to host localhost left intact
```

######error response
```bash
* upload completely sent off: 45 out of 45 bytes
< HTTP/1.1 400 Bad Request
< X-DNS-Prefetch-Control: off
< X-Frame-Options: SAMEORIGIN
< X-Download-Options: noopen
< X-Content-Type-Options: nosniff
< X-XSS-Protection: 1; mode=block
< Content-Type: application/json; charset=utf-8
< Content-Length: 223
< ETag: W/"df-H24GEQSG1qfcN7/dukmbkw"
< Date: Tue, 14 Feb 2017 09:28:36 GMT
< Connection: keep-alive
< 
* Connection #0 to host localhost left intact
[{"keyword":"uniqueAffiliateEmail","dataPath":".email","schemaPath":"#/properties/email/uniqueAffiliateEmail","params":{"keyword":"uniqueAffiliateEmail"},"message":"should pass \"uniqueAffiliateEmail\" keyword validation"}]
```

{% endmethod %}
