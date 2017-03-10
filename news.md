#News
Get available news.
##Endpoints
{% method %}
####`GET /news`

Get **last** 100 available news (use `offset` to get earlier news).
Use `types` param - one of `lists/news-types` - to select news by category and `search` param to search relevant news. Use `date_range` param to select news between needed dates.

{% sample lang="bash" %}
```bash
curl -X GET -v -b 'connect.sid=s%3AadtIeCZXVwjWFcGnsmw-BS3IVX6uhggo.a%2BvVlFq1keQhw%2F6Jlpjf4TeS%2BmTzfpbLjoM1RoDdDkc' 'http://dashboard.everad.com/v2/news' -H 'content-type: application/json' -d '{"types": ["new_offer", "offer_stop", "new_landing"], "offset": 100, "search": "your input"}' | jq .
```
######success response
```
< HTTP/1.1 200 OK
[
  {
    "published_at": "2017-03-01 09:42:26",
    "title": "test quos qui",
    "text": "Atque quia officia. Error et vel quae. Est temporibus libero nemo doloremque non consequuntur voluptates. Porro esse ipsum. Voluptatem vitae facilis est beatae corporis veniam. Voluptatem quia maiores omnis aut.\n \rQuia molestiae aut doloribus veritatis dolorem error porro sed reiciendis. Sit quae inventore voluptatem autem et incidunt et iure. Velit at et eius a impedit quam. Placeat minus officia possimus laborum maiores et alias consectetur maxime.\n \rQuos aut eos dolorem. Aliquam doloremque distinctio id libero explicabo consequatur ipsum vitae doloremque. Corporis possimus aut officiis. Quisquam omnis consequatur accusantium. Ea deserunt voluptatibus reiciendis aliquam commodi est fugiat. Voluptas repudiandae corrupti unde optio esse.",
    "type": "new_offer"
  }
]
```
{% endmethod %}