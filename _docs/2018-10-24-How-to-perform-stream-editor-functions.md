---
layout: single
title: "Command sed"
categories: Advanced Commands
date:   2018-10-24 13:31:20 +0200
---

## Command ```sed```
SED is a powerful text stream editor.
We can do insertion, deletion, search and replace(substitution).
We can use it to edit the file using the script.
In the script we can specify commands of one or more rows, in accordance with the rules that are listed as part of one or more commands.

Another option for sed command ```sed -e```
We use the sed -e command when we want to print the numbers of rows in which the specified pattern is found.

#### Example
{% highlight bash %}
sed -e "/ls/=" $1
{% endhighlight bash %}
