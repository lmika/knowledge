---
title: Lookups On A Nil Map
type: tidbit
---

You can do lookups on a `nil` map:

    var xs map[string]string = nil
    x, hasX := xs["hello"]

The result will simply be the zero value of the particular type. In this case `x` will be the empty string.