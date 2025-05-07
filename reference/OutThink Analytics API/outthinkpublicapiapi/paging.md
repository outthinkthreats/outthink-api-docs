---
title: Paging
deprecated: false
hidden: false
metadata:
  robots: index
---
Paging on the API is controlled by skip/take query parameters.

These parameters are optional, but they should be provided in all paged requests (unless only the default results set is required).

Skip rules:

* If not present, defaults to 0.
* Minimum value is 0, if a value lower than this is provided, skip will be set to 0.
* No upper limit.

Take rules:

* If not present, defaults to 10.
* Minimum value is 1, if a value lower than this is provided, take will be set to 1.
* Maximum value is 100, if a value greater than this is provided, take will be set to 100.