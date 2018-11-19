---
layout: post
title: Creating symbolic link
parent: Advanced Commands
nav_order: 3
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
