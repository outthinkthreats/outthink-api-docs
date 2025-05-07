---
title: Server Errors
deprecated: false
hidden: false
metadata:
  robots: index
---
All requests will contain a '*Correlation-Id*' response header with a unique value for each request. If you encounter any unexpected **500** errors, please attach this value to any support tickets raised with the support team.

If the incoming request already contains a *Correlation-Id* header, the api will return the client-supplied value as the *Client-Correlation-Id* response header.