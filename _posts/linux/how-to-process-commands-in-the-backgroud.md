---
layout: default
title:  Entering the commands that are processed in the background 
parent: Linux
nav_order: 8
---

## Entering the commands that are processed in the background

Shell provides the ability to handle commands in the background.
This is achieved by setting the ampersand symbol, &, to the end of the command.

{% highlight bash %}
find / -name "$1" -print > find.results 2>/dev/null &
{% endhighlight bash %}

