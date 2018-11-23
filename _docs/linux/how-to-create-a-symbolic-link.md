---
layout: single
title: Creating symbolic link
parent: Linux
permalink: /docs/linux/how-to-create-a-symbolic-link/
toc: true
---

{% include base_path %}


### Example for creating a symbolic link

{% highlight bash %}
touch slink
echo some_text > slink
ln -s slink some_text
cat slink
display output:
some_text
{% endhighlight bash %}
