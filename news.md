#News
Get available news.
##Endpoints
{% method %}
####`GET /news`

Get **last** 100 available news (use offset to get earlier news).
Use `type` param to select news by category and `search` param to search relevant news. 

{% sample lang="bash" %}
```bash
curl -X GET -v 'http://dashboard.everad.com/v2/news?offset=100&type=new_offer&search="test"'
```
######success response
```
< HTTP/1.1 200 OK
[
  {
    "id": 1,
    "created_at": "2017-01-31T23:02:40.842Z",
    "updated_at": "2017-02-07T04:55:38.728Z",
    "removed_at": null,
    "published_at": "2017-03-01T09:42:26.330Z",
    "title": "test quos qui",
    "text": "Atque quia officia. Error et vel quae. Est temporibus libero nemo doloremque non consequuntur voluptates. Porro esse ipsum. Voluptatem vitae facilis est beatae corporis veniam. Voluptatem quia maiores omnis aut.\n \rQuia molestiae aut doloribus veritatis dolorem error porro sed reiciendis. Sit quae inventore voluptatem autem et incidunt et iure. Velit at et eius a impedit quam. Placeat minus officia possimus laborum maiores et alias consectetur maxime.\n \rQuos aut eos dolorem. Aliquam doloremque distinctio id libero explicabo consequatur ipsum vitae doloremque. Corporis possimus aut officiis. Quisquam omnis consequatur accusantium. Ea deserunt voluptatibus reiciendis aliquam commodi est fugiat. Voluptas repudiandae corrupti unde optio esse.",
    "type": "new_offer"
  }
]
```
{% endmethod %}
