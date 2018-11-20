---
layout: default
title:  Entering multiple commands in one row
parent: Linux
nav_order: 9
---

## Enter multiple commands in one row
Usually, shell interprets the first word from the command input as the command name, and the rest of the input as an argument for that command.
A special shell character, a dot-comma (;), tells the shelf that the text of the previous command has ended and that what comes next behind this character is a new command.

### Example
{% highlight bash %}
find $1; ls $2; pwd $3
{% endhighlight bash %}
