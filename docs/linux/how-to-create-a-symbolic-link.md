---
layout: default
title: Creating symbolic link
parent: Linux
nav_order: 5
---


### Example for creating a symbolic link

{% highlight bash %}
touch slink
echo some_text > slink
ln -s slink some_text
cat slink
display output:
some_text
{% endhighlight bash %}
