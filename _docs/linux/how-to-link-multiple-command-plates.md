---
layout: single
title: Linking multiple commands
parent: Linux
permalink: /docs/linux/how-to-link-multiple-command-plates/
---

{% include base_path %}


## Linking multiple commands is achieved by using the symbol pipe, | .
When the shell sees the pipe, it executes the previous command and, after that, creates a link to the standard input of the following commands, in the order in which the commands a$

### Example

{% highlight bash %}
who | grep $1
{% endhighlight bash %}
