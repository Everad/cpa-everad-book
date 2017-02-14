# Session

manage your session section. Session data is passed over http cookie, returned to you on calling `login` or `register` endpoints

###Endpoints

{% method %}
`/session/register`

Register your affiliate account and get session cookie at once

{% sample lang="bash" %}
curl example.

```bash
curl -X POST -H 'Content-type: application/json' -d '{"email":"test2@example.com", "password":"1"}' -v http://localhost:4001/session/register
```
{% endmethod %}
