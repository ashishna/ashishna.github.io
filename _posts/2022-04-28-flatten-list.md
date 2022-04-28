---
layout: post
title: Flatten List and transform using closure
date: 2022-04-28 10:14 -0400
---

Groovy's `faltten` method can be used to merge all the nested collections into one single collection. The level of nesting does not matter. We can also pass closure to perform any transformation.

```groovy
def list = [[1,2,3], [4], [[5,6]]]

assert list.flatten() == [1, 2, 3, 4, 5, 6]

// Use closure to perform any transformations
assert list.flatten { it * 2 } == [2, 4, 6, 8, 10, 12]
```
