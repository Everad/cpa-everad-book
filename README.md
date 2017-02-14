# Everad CPA v2 Dashboard API

This describes **API** for managing your affiliate account inside **Everad CPA** application.

API operates **REST** principles with some deviations described explicitly in method's description.

All incoming data is passed using **JSON** format (with specified `Content-type: application/json` header)

####Response usable data:
**HTTP Status Code** indicates whether your request was successfuly processed (`200`, `201` codes) or ended with error (`400` - bad income data, `403` - you have no permission to access requested endpoint, `500` - internal server error, need to contuct support)

**Response Body** contains requested or error info (for `400` status codes)

####Base url
 `http://dashboard.everad.com`

#### Methods available:
`/lists` - fetch available data enums, used in other endpoints
`/session` - manange your current session and access permissions to internal methods
`/profile` - manage profile data (contacts, payments, language info)
`/news` - fetch current news
`/offers` - fetch available offers, manage your current offer permissions
`/spaces` - manage your personal spaces for groupping your incoming traffic
`/campaigns` - manage your campaigns
`/support` - manage your support requests



