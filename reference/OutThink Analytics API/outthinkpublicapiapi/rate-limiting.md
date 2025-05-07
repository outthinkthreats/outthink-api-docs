---
title: Rate Limiting
deprecated: false
hidden: false
metadata:
  robots: index
---
Each individual client (as identified by the value on *OT-Customer-Id*) is allowed up to 10 requests per second on the api.

Going above that will trigger a 429 response with a recommended wait time.