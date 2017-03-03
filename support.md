#Support
Retrieve your communication with support.

##Endpoints
{% method %}
####`GET /threads`

Get a list of your threads.

{% sample lang="bash" %}
```bash
curl -X GET -v -b 'connect.sid=s%3A7OKmdhfZr6qJ_H5OWLKJCRWfyoWAtm6q.yzfCuK0Flvj5xW8UlRES3JTyZNMGLhiTF8aPEZ3MFOo' 'http://dashboard.everad.com/v2/threads'
```
######success response
```
< HTTP/1.1 200 OK
[
  {
    "created_at": "2017-03-02 15:07:51",
    "updated_at": "2017-03-02 15:07:51",
    "status": "active",
    "category": "affiliate_question",
    "priority": "critical",
    "title": "умысел иллюстрирует продукт",
    "offer_title": null
  },
  {
    "created_at": "2017-03-02 15:07:51",
    "updated_at": "2017-03-02 15:07:51",
    "status": "active",
    "category": "new_landing_transit",
    "priority": "high",
    "title": "панладовая верлибр однородно",
    "offer_title": "maiores a provident"
  },
  {
    "created_at": "2017-03-02 15:36:01",
    "updated_at": "2017-03-02 15:36:01",
    "status": "active",
    "category": "offer_access",
    "priority": "normal",
    "title": "ревер индивидуально Банкротство",
    "offer_title": "sapiente et enim"
  }
]
```
{% endmethod %}
{% method %}
###`GET /threads/:id`
Get posts within a thread by its id.
{% sample lang="bash" %}
```bash
curl -X GET -v -b 'connect.sid=s%3A09OpKmlx3UY73RKvuKH1-KpaorJNxuwN.GMThTayHUQ0kjmztr4Gf4xIjrs%2FQcJXJAzTabTELFuM' 'http://dashboard.everad.com/v2/threads/2'
```
######success response
```
< HTTP/1.1 200 OK
[
  {
    "created_at": "2017-02-20 09:35:32",
    "updated_at": "2017-02-20 09:35:32",
    "text": "Пуанта нуждается определению артиста Представленный Веселых. Хотя среда рассматривать несостоятельно. В известно но устного медиавес. Гипноз экзистенциальный индуцирует.",
    "author": "affiliate"
  },
  {
    "created_at": "2017-02-21 09:32:32",
    "updated_at": "2017-02-21 09:32:32",
    "text": "Осознаёт англо-саксонской институциональный штраф провоз. Преимущества известно перспективной Инвестиционный собак понимает своей. Продукт психолингвистическим в.",
    "author": "admin"
  },
  {
    "created_at": "2017-02-22 01:20:31",
    "updated_at": "2017-02-22 01:20:31",
    "text": "Этот панладовая начинает иллюстрирует является практически фактура. Понимает Потехина Как эриксоновский чувствовал Весьма. Баинг Пуанта осознаёт.",
    "author": "affiliate"
  }
]
```
{% endmethod %}
{% method %}
###`POST /threads`
Create a thread.
{% sample lang="bash" %}
```bash
curl -X POST -v -H 'Content-type: application/json' -b 'connect.sid=s%3A9RnpiJ4u9OE2WWFHGLG49jP01sTScNFq.WrmLKZAsFsVO1OkDvAaurzdeQnQMOeKOpvbZADY%2B5m8' -d '{"title":"i want offer access", "priority": "critical", "offer_id": 10, "category": "offer_access", "text": "please give me access to this order thanks"}' http://dashboard.everad.com/v2/threads
```
######success response
```
< HTTP/1.1 201 Created
```
{% endmethod %}
{% method %}
###`POST /threads/:id`
Create a post in a thread.
{% sample lang="bash" %}
```bash
curl -X POST -v -b 'connect.sid=s%3AVvfflLue_6MkfHEN5S9N2tN9-z50Zdxf.ASQBDXkdlsoRIklt6ltLiEGGdr%2BtawqRF%2BhLX51apbg' 'http://dashboard.everad.com/v2/threads/15' -H 'Content-type: application/json' -d '{ "text": "post text here" }'
```
######success response
```
< HTTP/1.1 201 Created
```
{% endmethod %}