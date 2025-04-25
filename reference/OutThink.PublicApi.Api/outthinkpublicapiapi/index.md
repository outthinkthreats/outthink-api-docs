---
title: OutThink.PublicApi.Api
hidden: false
---
# Authentication

All requests must include both a client identification header and authorization API key. They identify the callertenant and authorize access to the API sub-sections respectively.

<br />

**Client identification:** `OT-Customer-Id: {uniqueValue}`

**Authorization:** `Authorization: Bearer {apiKey}`

*Please ensure the Bearer scheme is set.*

The unique client identification header and a set of primary/secondary api keys will get provided by the OutThink Team.

Failure to include some of these headers, or using invalid values will trigger a **400** response with one of the following codes:

* `missing_customer_id_header`
* `invalid_customer_id_header`
* `missing_authorization_header`
* `invalid_authorization_header`

## Rate Limiting

Each individual client (as identified by the value on *OT-Customer-Id*) is allowed up to 10 requests per second on the api.

Going above that will trigger a 429 response with a recommended wait time.