#Lookups
{% method %}
####`GET /lookups/offers`
Return 5 results based on query. Only offers, available for campaign creation, can be returned.
**Params:**
`title` - title part (min 1 symbol)
`lang` - optional parameter. Profile language used by default

{% sample lang="bash" %}
```bash
curl -X GET -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' -v http://dashboard.everad.com/v2/lookups/offers?title=intox
```
######success response
```
< HTTP/1.1 200 OK
[{"id":"1","text":"intoxic"},{"id":"2","text":"intoxic+"}]
```

{% endmethod %}
