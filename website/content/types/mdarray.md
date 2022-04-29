---
sidebar_position: 7
title: MDArray
---

MDArray stands for Multi Dimentional Array. The dimentionality of the array cannot be changed after it's creation. There are two ways of initiating an MDArray. The first is to provide it's initial size and number of dimentions. The way is providing the exact values that the array is going to contain.

```acl
a = |2, 3, 4|
b = |||0, 0, 0, 0|, |0, 0, 0, 0|, |0, 0, 0, 0||, ||0, 0, 0, 0|, |0, 0, 0, 0|, |0, 0, 0, 0|||

print a == b // true
