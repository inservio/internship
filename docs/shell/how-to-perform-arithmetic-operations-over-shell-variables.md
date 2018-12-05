---
layout: default
title: Perform arithmetic operations over shell variables
parent: Shell
permalink: /docs/shell/how-to-perform-arithmetic-operations-over-shell-variables/
---

# Introduction

Variables are typed in most programming languages, which means they are limited to certain types of data, such as numbers or characters. Shell variables are always remembered as $

expr integer operator integer

The following operators are the important arithmetic operators:
(+)Sets two whole numbers

(-)It subtracts the second full integer from the first full integer.

(*) There are two integer numbers (When we want to multiply two integers in the terminal we have to use the correct format for multiplication, which is "expr 4 * 5")

(/) The first integer is shared by another integer.

(%) Gives the module (rest) of the sharing.

## Demonstration

### Examples

Example arithmetic addition operation + "
Example 2 + 1

```expr 2 + 1```

Example arithmetice subtraction - "
Example 5 - 4

```expr 5 - 4```

Example arithmetic multiplication operation * but the the correct form of multiplication in the terminal is \* "
Example 7 \* 8"

```expr 7 \* 8```

Example arithmetic division operation / "
Example 6 / 2

```expr 6 / 2```

Arithmetic terms can also be combined, as in the following example:
Example 6 + 7 / 3
```expr 6 + 7 / 3```

Command expr does not recognize brackets, which is why you need to manually override the priority, if there is a need for it.
We can use backward characters to change priority rights, in the following way:
Example
```int = expr 6 + 7```
```expr int / 3```

```int= `expr 6 + 7` ```
```expr $int / 3```

Or we can use a more direct route:
Example expr 6 + 7' / 3

```expr `expr 6 + 7` / 3```
