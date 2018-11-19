---
layout: post
title: Linking multiple commands
parent: Advanced Commands
date:   2018-10-4 13:31:20 +0200
---

Linking multiple commands is achieved by using the symbol pipe, | .
When the shell sees the pipe, it executes the previous command and, after that, creates a link to the standard input of the following commands, in the order in which the commands a$

### Example

{% highlight bash %}
who | grep $1
{% endhighlight bash %}
