---
layout: post
title:  "Groovier: Drop or take characters from String in Groovy"
date:   2022-04-26 11:29:26 -0400
categories: groovy
tags: groovy code string howto java
---

# Groovy String 

Groovy has added many methods in String class which can be used to `drop` or `take` part of `String` from begining of the String.


```groovy
def str = "Groovy is awesome !"

assert "is awesome !" ==  str.drop(7)

assert "s awesome !" == str.dropWhile { it != 's'}

assert "Groovy" ==  str.take(6)

//Keep taking the string until character ! is reached.
assert "Groovy is awesome " == str.takeWhile  { it != '!'} 
```