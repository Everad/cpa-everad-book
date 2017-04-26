#Campaigns
Manage your campaigns. ***TODO add split sessions***
##Endpoints
{% method %}
###`GET /campaigns`
Get your campaigns.
{% sample lang="bash" %}
```bash
curl -X GET -v -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' http://dashboard.everad.com/v2/campaigns
```
######success response
```
[{
    id
    created_at
    updated_at
    title
    is_active - flag indicating that campaign can receive traffic
    offer_id
    space_id
    currency - one of /lists/currencies
    postback_url
    postback_type - one of /lists/postback-types
    postback_ignore_trash - flag
    trafficback_url
    landing_domain
    landing_domain_type - one of /lists/campaign-domain-types
    transit_domain
    transit_domain_type - one of /lists/campaign-domain-types
    traffic_source - one of /lists/traffic-sources
    sid1_utm
    sid2_utm
    sid3_utm
    sid4_utm
    sid5_utm
    is_novostnik_on_transit_enabled
    is_novostnik_after_submit_enabled
    is_comebacker_enabled,
    domains: [{
        id -  one of /offers/<id> domains.id
    }],
    adv_system - one of /lists/adv-systems,
    landings_snippets_codes: {
        landing: [{id: 1, text: 'code'}], - id = external_id from /lists/landings-snippets
        transit: [{id: 1, text: 'code'}]
    } 
}]
```
{% endmethod %}
{% method %}
###`GET /campaigns/<id>`
Get a campaign by id.
{% sample lang="bash" %}
```bash
curl -X GET -v -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' http://dashboard.everad.com/v2/campaigns/1
```
######success response
```
< HTTP/1.1 200 OK
{
    id
    created_at
    ...
}
```
{% endmethod %}
{% method %}
###`POST /campaigns`
Create a new campaign (required fields are marked with `*`).
```
*title
*offer_id - one of /offers with an `available` flag set to true
space_id - one of /spaces
postback_url
postback_type - one of /lists/postback-types
trafficback_url
*landing_domain - if local, should end with one of /lists/campaign-domains.
*landing_domain_type - one of /lists/campaign-domain-types
transit_domain - if local, should end with one of /lists/campaign-domains.
transit_domain_type - one of /lists/campaign-domain-types
sid1_utm
sid2_utm
sid3_utm
sid4_utm
sid5_utm
is_novostnik_on_transit_enabled
is_novostnik_after_submit_enabled
is_comebacker_enabled
*domains: [{
    *id - one of /offers/<id> domains.id   
}],
*adv_system - one of /lists/adv-systems,
landings_snippets_codes: {
    landing: [{id: 1, text: 'code'}], - id = external_id from /lists/landings-snippets
    transit: [{id: 1, text: 'code'}]
}
```

{% sample lang="bash" %}
```bash
curl -X POST -v -H 'Content-type: application/json' -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' -d '{"offer_id": 1, "landing_domain": "google.com", "landing_domain_type": "external", "domains": [{"id": 1}], "adv_system": "other"}' http://dashboard.everad.com/v2/campaigns
```
######success response
```
< HTTP/1.1 201 Created
```
{% endmethod %}
{% method %}
###`PUT /campaigns/<id>`
Update an existing campaign. Input fields are the same as when creating a new campaign.
{% sample lang="bash" %}
```bash
curl -X PUT -v -H 'Content-type: application/json' -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' -d '{"offer_id": 1, "landing_domain": "google.com", "landing_domain_type": "external"}' http://dashboard.everad.com/v2/campaigns/1
```
######success response
```
< HTTP/1.1 200 OK
```
{% endmethod %}
{% method %}
###`DELETE /campaigns/<id>`
Remove a campaign.
{% sample lang="bash" %}
```bash
curl -X DELETE -v -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' http://dashboard.everad.com/v2/campaigns/1
```
######success response
```
< HTTP/1.1 200 OK
```
{% endmethod %}