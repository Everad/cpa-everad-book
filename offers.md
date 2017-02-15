#Offers
List available offers
##Endpoints
{% method %}
####`GET /offers`

Get available offers. Availability is marked over `available` flag. If it's `true` - you can create campaign with this offer. Otherwise access request required (look at support section).
{% sample lang="bash" %}
```bash
curl -X GET -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' -v http://dashboard.everad.com/v2/offers
```
######success response
```
[{
    id
    title
    category - one of /lists/offer-categories
    short_description
    description
    rules
    domain
    is_exclusive
    locations: [
        name
        is_own_callcenter
        price
        currency - one of /lists/currencies
    ],
    domains: [{
        id
        type - one of /lists/domain-types
        title
        domain
    }],
    payouts: [{
        location - location name
        traffic_type - one of /lists/traffic-types
        traffic_source - one of /lists/traffic-sources
        currency - one of /lists/currencies
        amount
    }]
}]
```
{% endmethod %}
{% method %}
####`GET /offers/<id>/news`
Get offer news
{% sample lang="bash" %}
```bash
curl -X GET -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' -v http://dashboard.everad.com/v2/offers/1/news
```
######success response - same as general news

{% endmethod %}

