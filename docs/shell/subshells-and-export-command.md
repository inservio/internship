---
layout: default
title: Subshells and export command        
parent: Shell
permalink: /docs/shell/subshells-and-export-command/
---

# Introduction

When a shell executes a program, it sets a new environment.
It is called subshell.
In the shell variables are viewed as local, in other words, they can not be recognized outside the shell, in which they were assigned value.
You can make the variable available to any subshells you run by exporting it with the export command.
Your variables can not be made available to other users.

In algebra, variables are symbols that represent some value.
In computer terminology, variables are symbolic names that represent some value.
Variables are useful in every computer language, because they allow you to define what needs to be done with information, without knowing the data.
Shell has four types of variables:
-Variables defined by the user
-Position variables, or shell arguments
-Previously defined, or specific variables
-Variable environment

Variables defined by the user are all that you want to be.
The variable names are composed of alphanumeric characters and underscores, provided that the names of the variables can not start from a digit from 0 to 9. Like all Linux names, t$
The variables have the values when in the command line they are left of the equals sign (=).

## Demonstration

### Example

{% highlight ruby %}

NAME=Adi
echo Hello $NAME```

Display the output

Adi
{% endhighlight ruby %}

{% highlight ruby %}
JOHN=John
NAME=$JOHN
PAGE=Page
SURNAME=$PAGE
NAME_AND_SURNAME=$NAME$SURNAME
echo My name and my last name is ${NAME} ${SURNAME}
Display the output
My name and my surname is John Page
{% endhighlight ruby %}
