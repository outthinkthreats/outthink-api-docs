---
title: Authentication
deprecated: false
hidden: false
metadata:
  robots: index
---
## Authentication

All requests must include both a client identification header and authorization api key. They identify the caller tenant and authorize access to the API sub-sections respectively.

**Client identification:** `OT-Customer-Id: {uniqueValue}`

**Authorization:** `Authorization: Bearer {apiKey}`

*Please ensure the Bearer scheme is set.*

The unique client identification header and a set of primary/secondary api keys will get provided by the OutThink Team.

Failure to include some of these headers, or using invalid values will trigger a **400** response with one of the following codes:

* `missing_customer_id_header`
* `invalid_customer_id_header`
* `missing_authorization_header`
* `invalid_authorization_header`