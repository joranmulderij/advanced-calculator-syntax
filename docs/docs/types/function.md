---
sidebar_position: 4
title: Function
---

Functions in ACL are very similar to functions in other programming languages. They are variables and can be passed as parameters. The following code shows how to define a function:

```acl
f(x) = x^2 - 2x + 1

g(x) = f'(x)
g = f'

h(x) = f(x) * g(x)
h = f*g

i(x) = f(x) ^ g(x)
i = f ^ g
```
