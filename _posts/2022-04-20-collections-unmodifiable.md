---
layout: post
title: "Groovy: Create unmodifiable list"
date: 2022-04-28 10:14 -0400
categories: groovy
tags: groovy code list filter how-to java
---

We can also use `asImmutable()` method on list to make an unmodifiable list.

```groovy
// Create List that is unmodifiable.
def list = ["Sun", "Earth", "Pluto", "Jupiter"].asImmutable()

// This will throw UnsupportedOperationException when try to modify the list
list << "Summary"
```