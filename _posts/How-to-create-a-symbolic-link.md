---
layout: post
title: Creating symbolic link
parent: Advanced Commands
date:   2018-10-4 13:31:20 +0200
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
