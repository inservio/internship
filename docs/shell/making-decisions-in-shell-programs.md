---
layout: default
title: Making decisions in shell programs
parent: Shell
permalink: /docs/shell/making-decisions-in-shell-programs/
---
# Introduction

One of the advantages that gives computer programming languages great power is their ability to make decisions.
Of course, computers are not able to think, so the decisions that programs bring on the computer represent only the answer to the conditions that you predicted in your program.
Decisions made by programs on the computer are in the form of conditional execution:
-if there is a requirement, then a specific set of commands is executed.
In most computer languages, this command is called if-then construction.

## Demonstration

### Example for if-then construction
Command if-then example
Combine the command ls -a -l and display the length of the list.

{% highlight ruby %}
if ls
then
ls -a
ls -l
fi
{% endhighlight ruby %}
