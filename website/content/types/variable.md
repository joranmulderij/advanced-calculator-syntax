---
sidebar_position: 1
title: Variable
---

Variables in ACL are completely different from variables in other programming languages. In ACL, variables do not nessecarily need to have a value. It only contains constraints. If a variable has enough constriants, it might obtain a value, but this does not need to happen. I may also be constraint to a list of values, a range of values, multiple ranges, all possitive numbers, all imaginary numbers, all real numbers, etc.

Here is a simple example of how you would be able to use variables:

```acl
var x
def 35x = 5
print x // 7
```

Variables cannot be re-asigned. Trying to do so will only add more constraints to the variable. To "reset" a variable, you need to delete it:

```acl
del x
```

Alternatively the `delall` statement may be used to delete all the variables.

## Internal working

The variable object is the most complex type in the list. It might also be the most useful, providing one of the gateways to this language's CAS functionality.

Internally the variable object collects a range of different "constraints". There are 3 types:

* Function constraint. These can be made by defining an equation.
* Range constraint. defining that a variable is in a certain range.
* Fundemental constraints. These include stating that a variable is an integer, is real, is rational etc.

Functional constraints are functions in the form of `f(x) = [expressions with optional variables]`.

When an equation get defined, the program will isolate all of the variables in the equasion seperately, and will asign the function constraint to it's respective `variable`.

When a constraint gets added to a variable, the variable will check if it's definitive value can be updated with the new information.

