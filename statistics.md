#Analytics
Get your traffic and conversions statistics
{% method %}
###`POST /analytics/general`
Get date ranged general statistics

**Query parameters:**




`lang` - desired response language (session language by default)

**Body parameters:**

```
date_range: { -- desired date range (with correct hours, e.g. end of day: 23:59:59.999999)
    start
    end
},

groups: ['date', 'hour', 'offer', 'landing', 'transit', 'country', 'city', 'campaign', 'campaign_type', 'traffic_type', 'sid1', 'sid2', 'sid3', 'sid4', 'sid5'], -- several values available
filters: {
    offers: [ids] -- one of /analytics/lists/offers,
    landings: [ids] -- one of /analytics/lists/landings, 
    transits: [ids] -- one of /analytics/lists/transits, 
    countries: [ids] -- one of /analytics/lists/countries,
    cities: [ids] -- one of /analytics/lists/cities, 
    campaigns: [ids] -- one of /analytics/lists/campaigns, 
    campaign_types: [types] -- one of /lists/campaign-types,
    traffic_types: [types] -- one of /lists/traffic-types, 
    sids1: [sid1] -- one of /analytics/lists/sids1, 
    sids2: [sid2] -- one of /analytics/lists/sids2, 
    sids3: [sid3] -- one of /analytics/lists/sids3, 
    sids4: [sid4] -- one of /analytics/lists/sids4, 
    sids5: [sid5] -- one of /analytics/lists/sids5
}
```

{% sample lang="bash" %}
```bash
curl -v -X POST -H 'Content-type: application/json' -d'{"date_range": {"start": "2017-01-01", "end": "2017-02-23 23:59:59.99999"},"groups": ["offer"], "filters": {"landings": [5]}}' -b 'connect.sid=s%3AvJyC27a4pDMt58b2m_7BNyW4FD9Y0UUG.gbDlAoNjiOA8jmBHC68FCWzoLtYA0Cw9xVRuzErQXAA' http://dashboard.everad.com/v2/analytics/general?lang=ru
```
######success response
```
< HTTP/1.1 200 OK
[{"hosts":"6","hits":"6","transitions":"0","accepted_conversions":"0","pending_conversions":"2","declined_conversions":"0","total_conversions":"2","invalid_conversions":"0","accepted_income":"0","pending_income":"200.00","declined_income":"0","offer":"beer"}]
```
{% endmethod %}
