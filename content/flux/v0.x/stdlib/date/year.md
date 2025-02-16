---
title: date.year() function
description: >
  The `date.year()` function returns the year of a specified time.
aliases:
  - /influxdb/v2.0/reference/flux/functions/date/year/
  - /influxdb/v2.0/reference/flux/stdlib/date/year/
  - /influxdb/cloud/reference/flux/stdlib/date/year/
menu:
  flux_0_x_ref:
    name: date.year
    parent: date
weight: 301
introduced: 0.39.0
---

The `date.year()` function returns the year of a specified time.

```js
import "date"

date.year(t: 2019-07-17T12:05:21.012Z)

// Returns 2019
```

## Parameters

### t {data-type="time, duration"}
The time to operate on.
Use an absolute time, relative duration, or integer.
Durations are relative to `now()`.

## Examples

##### Return the year for a time value
```js
import "date"

date.year(t: 2020-02-11T12:21:03.293534940Z)

// Returns 2020
```

##### Return the year for a relative duration
```js
import "date"

option now = () => 2020-02-11T12:21:03.293534940Z

date.year(t: -14y)

// Returns 2006
```
