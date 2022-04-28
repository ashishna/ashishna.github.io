---
layout: post
title: "Groovier: Implement interface in Groovy using closure"
date: 2022-04-26 13:53 -0400
categories: groovy
tags: groovy code list filter howto java
---

Groovy's `closure` can be used to implement the interfaces with pretty ease. This can come handy when creating scaffolding of code or creating mocks for testing.


## Single method interface with same implementation

```groovy
interface AwesomeInterface {
    void x(String x)
    void y()
}

def interfaceImpl = 
    { String str -> println("Implementation of methods of interface with value: ${str}") } as AwesomeInterface

interfaceImpl.x("Awesome")
interfaceImpl.y() // will call same implementation with null arguments
```

## Output

```text
Implementation of methods of interface with value: Awesome
Implementation of methods of interface with value: null
```

## Multiple methods implementation in an interface

```groovy
interface AwesomeInterface {
    void x(String x)
    void y()
}
// Use Map as method name as key and Closure as an argument with the implementation 
def interfaceImpl = [
    x: { String str -> println("Implementation method x() of interface with argument: ${str}") },
    y: { println("Implementation of method y() of interface") }
        ] as AwesomeInterface
interfaceImpl.x("Awesome")
interfaceImpl.y() 
```

## Output

```text
Implementation method x() of interface with argument: Awesome
Implementation of method y() of interface
```