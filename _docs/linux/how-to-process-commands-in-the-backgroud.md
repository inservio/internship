---
layout: single
title:  Entering the commands that are processed in the background
parent: Linux
permalink: /docs/linux/how-to-process-commands-in-the-backgroud/
toc: true
---

{% include base_path %}


## Entering the commands that are processed in the background

Shell provides the ability to handle commands in the background.
This is achieved by setting the ampersand symbol, &, to the end of the command.

{% highlight bash %}
find / -name "$1" -print > find.results 2>/dev/null &
{% endhighlight bash %}
