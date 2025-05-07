---
title: Data Validation And Error Responses
deprecated: false
hidden: false
metadata:
  robots: index
---
Unless explicitly specified in an operation, all argument names, filtering attributes, etc., must be considered  **case-insensitive**.

Some endpoints may have mandatory and/or optional parameters. If a value doesn't pass validation, or is missing in a mandatory parameter, it will trigger a **400 BAD REQUEST** response with the following payload:

```json
{ 
    "code": "missing_parameter", 
    "field": "orgId", 
    "reason": "Required paramater 'orgId' not supplied in the request"
}
```

* `code`: Unique error code.
* `field`: Name of the argument or field that caused the error.
* `reason`: Human-friendly description, in english text. Might change without warning or not be unique between different errors, always rely on `code` for error identification.

Common error codes thrown during data validation:

* `missing_parameter`: Mandatory parameter not included in the request.
* `invalid_parameter`: Parameter was not in the proper format