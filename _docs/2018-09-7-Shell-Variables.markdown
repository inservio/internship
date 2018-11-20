---
layout: single
title:  "Shell Variables!"
date:   2018-10-4 13:31:20 +0200
categories: sv
---

## Position variables, or shell arguments

When a shell interpreter handles the input order, it considers the first word in the command line as an executable file, and the rest of the line as arguments that it passes to an executable file.
If an executable file is a shell program, these arguments are passed to that program as position variables.
The first argument given to the program is assigned to the $ 1 variable, the second argument is $ 2 and so on, up to $ 9.
We can observe that the names of the variables, in fact, the digits 1 to 9, the dollar sign is, as always, a special character that causes the replacement of the variable.
The $ 0 position variable always contains the name of the program.

## Prevent changing the variable

If a variable is assigned a value, and you want to be sure that no later changes will be made.
Using the following command, you can specify that the variable is the read-only variable:
```readonly $1```

## Subshells and export command

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
The variable names are composed of alphanumeric characters and underscores, provided that the names of the variables can not start from a digit from 0 to 9. Like all Linux names, the variables are case-sensitive.
The variables have the values when in the command line they are left of the equals sign (=).

Example
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
