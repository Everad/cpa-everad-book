#Lists
endpoints for receiving different lists, used by other parts of API
##Endpoints
{% method %}
###`GET /lists/languages`
retrieve available response languages
{% sample lang="bash" %}
```bash
curl -X GET -v http://dashboard.everad.com/v2/lists/languages
```
######success response
```
< HTTP/1.1 200 OK
["en","ru","ro","th"]
```
{% endmethod %}
{% method %}
###`GET /lists/space-types`
{% endmethod %}
{% method %}
###`GET /lists/offer-categories`
{% endmethod %}
{% method %}
###`GET /lists/currencies`
{% endmethod %}
{% method %}
###`GET /lists/campaign-domains` - available only for active session
{% endmethod %}
{% method %}
###`GET /lists/domain-types`
{% endmethod %}
{% method %}
###`GET /lists/traffic-types`
{% endmethod %}
{% method %}
###`GET /lists/traffic-sources`
{% endmethod %}





