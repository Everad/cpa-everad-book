#Campaigns
manage your campaigns ***TODO add split sessions***
##Endpoints
{% method %}
###`GET /campaigns`
Get your campaigns
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
    is_active - flag indicating that campaign can recieve traffic
    offer_id
    space_id
    postback_url
    postback_type - one of /lists/postback-types
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
        id -  one of /offers/ .<id>.domains
    }]
}]
```
{% endmethod %}
{% method %}
###`POST /campaigns`
Create new campaign (requred fields marked by `*`)
```
*offer_id - one of /offers with `available` flag active
space_id - on of /spaces
postback_url
postback_type - one of /lists/postback-types
trafficback_url
*landing_domain
*landing_domain_type - one of /lists/campaign-domain-types
*transit_domain
*transit_domain_type - one of /lists/campaign-domain-types
sid1_utm
sid2_utm
sid3_utm
sid4_utm
sid5_utm
is_novostnik_on_transit_enabled
is_novostnik_after_submit_enabled
is_comebacker_enabled
*domains: [{
    *id - one of /offers .<id>.domains.id   
}]
```

{% sample lang="bash" %}
```bash
curl -X POST -v -b 'connect.sid=s%3AL7xQwNemYqilwERqH8tswYKfk6XfqcaC.P4qkrt3mUix3Dw6A2ze7Z9phswc%2FHIKqGYZ4YJyLYE0' http://dashboard.everad.com/v2/campaigns
```
######success response

{% endmethod %}
