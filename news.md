#News
Get available news
##Endpoints
{% method %}
####`GET /news`

Get **last** 100 available news (can use offset to get other pages)
{% sample lang="bash" %}
```bash
curl -X GET -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' -v http://dashboard.everad.com/v2/news?offset=100
```
######success response
```
< HTTP/1.1 200 OK
[{"published_at":"2017-02-14T11:28:43.646Z", "text":""
title
:
"Расширение гео на оффере Valgulex - средство от вальгусной деформации"}]
```
{% endmethod %}
