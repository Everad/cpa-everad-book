#Lists
Endpoints for receiving different lists, used by other parts of API. 

Use `?lang=ru` or `?lang=en` query parameters in the URL to explicitly request localized versions of lists. English is set by default unless your browser language or your user profile language are supported by the API.
##Endpoints
{% method %}
###`GET /lists/languages`
Retrieve available response languages.
{% sample lang="bash" %}
```bash
curl -X GET -v http://dashboard.everad.com/v2/lists/languages
```
######success response
```
< HTTP/1.1 200 OK
[{"id":"en","text":"English"},{"id":"ru","text":"Russian"}]
```
{% endmethod %}
{% method %}
###`GET /lists/space-types`
Retrieve possible space types.
{% sample lang="bash" %}
```bash
curl -X GET -v http://dashboard.everad.com/v2/lists/space-types
```
######success response
```
< HTTP/1.1 200 OK
[{"id":"site","text":"site"},{"id":"context","text":"context"},{"id":"social","text":"social"},{"id":"doorway","text":"doorway"},{"id":"email","text":"email"},{"id":"arbitrage","text":"arbitrage"}]
```
{% endmethod %}
{% method %}
###`GET /lists/offer-categories`
Retrieve possible offer categories.
{% sample lang="bash" %}
```bash
curl -X GET -v http://dashboard.everad.com/v2/lists/offer-categories
```
######success response
```
< HTTP/1.1 200 OK
[{"id":"slimming","text":"slimming"},{"id":"cosmetics","text":"cosmetics"},{"id":"adult","text":"adult"},{"id":"medical","text":"medical"},{"id":"auto","text":"auto"},{"id":"other","text":"other"}]
```
{% endmethod %}
{% method %}
###`GET /lists/currencies`
Retrieve available currencies.
{% sample lang="bash" %}
```bash
curl -X GET -v http://dashboard.everad.com/v2/lists/currencies
```
######success response
```
< HTTP/1.1 200 OK
[{"id":"usd","text":"usd"},{"id":"rub","text":"rub"},{"id":"byn","text":"byn"},{"id":"kgs","text":"kgs"},{"id":"kzt","text":"kzt"},{"id":"mdl","text":"mdl"},{"id":"azn","text":"azn"},{"id":"gel","text":"gel"},{"id":"uah","text":"uah"},{"id":"ron","text":"ron"},{"id":"thb","text":"thb"},{"id":"amd","text":"amd"}]
```
{% endmethod %}
{% method %}
###`GET /lists/campaign-domains` - available only for active session
{% sample lang="bash" %}
```bash
curl -X GET -b 'connect.sid=s%3AWt1ZtB7mMKQCcTAVs7_iPVQ5-EU6o_0Q.0aMir6l0Raw%2BCJrZYPoAWQM1ATFWhUX2VxgYL%2FuqEy0' -v http://dashboard.everad.com/v2/lists/campaign-domains
```
######success response
```
< HTTP/1.1 200 OK
[{"id":1,"text":"example.com"},{"id":2,"text":"example.com"}]
```

{% endmethod %}
{% method %}
###`GET /lists/offer-domain-types`
Retrieve possible offer domain types.
{% sample lang="bash" %}
```bash
curl -X GET -v http://dashboard.everad.com/v2/lists/offer-domain-types
```
######success response
```
< HTTP/1.1 200 OK
[{"id":"landing","text":"landing"},{"id":"transit","text":"transit"}]
```
{% endmethod %}
{% method %}
###`GET /lists/timezones`
Retrieve possible system timezones.
{% sample lang="bash" %}
```bash
curl -X GET -v http://dashboard.everad.com/v2/lists/timezones
```
######success response
```
< HTTP/1.1 200 OK
[{"id":"Europe/Moscow","text":"Europe/Moscow"},{"id":"Europe/Minsk","text":"Europe/Minsk"}]
```
{% endmethod %}
{% method %}
###`GET /lists/traffic-types`
Retrieve possible system traffic types.
{% sample lang="bash" %}
```bash
curl -X GET -v http://dashboard.everad.com/v2/lists/traffic-types?lang=ru
```
######success response
```
< HTTP/1.1 200 OK
[{"id":"desktop","text":"компьютер"},{"id":"tablet","text":"планшет"},{"id":"phone","text":"смартфон"},{"id":"bot","text":"бот"},{"id":"tv","text":"телевизор"}]
```
{% endmethod %}
{% method %}
###`GET /lists/campaign-types`
Retrieve possible system campaign types.
{% sample lang="bash" %}
```bash
curl -X GET -v http://dashboard.everad.com/v2/lists/campaign-types?lang=ru
```
######success response
```
< HTTP/1.1 200 OK
[{"id":"general","text":"общий"},{"id":"novostnik","text":"с новостника"},{"id":"parked_novostnik","text":"с паркованного новостника"}]
```
{% endmethod %}

{% method %}\
###`GET /lists/news-types`
Retrieve possible news types.
{% sample lang="bash" %}
```bash
curl -X GET -v http://dashboard.everad.com/v2/lists/news-types?lang=ru
```
######success response
```
< HTTP/1.1 200 OK
[{"id":"new_offer","text":"новинки"},{"id":"offer_stop","text":"приостановка офферов"},{"id":"offer_change","text":"изменение офферов"},{"id":"geo_change","text":"расширение гео"},{"id":"new_landing","text":"новые лэндинги"},{"id":"custom","text":"системные тикеты"}]
```
{% endmethod %}


















































































