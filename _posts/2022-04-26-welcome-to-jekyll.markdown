---
layout: post
title:  "How to filter list in Groovy"
date:   2022-04-26 11:29:26 -0400
categories: groovy code 
---

## To filter a list in groovy we can use the `.find()` method on list and pass the closure as filtering criteria

Sample code snippets below


### `.find()` - To find a single value matching the critetia. Use `findAll()` for multiple values

```groovy
def lst = ["apple", "banana", "mangos"]
lst.find { it == "apple"} // Get only apple
```

### Output
```text
Result: banana
```

### `findAll()` - to find multiple results and filter nulls

```groovy
def lstWithNulls = ["John", "Sonia", null, "David", "Andrew", null]
lstWithNulls.findAll()
```

### Output
```text
Result: [John, Sonia, David, Andrew]
```
