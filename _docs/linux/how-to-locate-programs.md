---
layout: single
title:  Command whereis
parent: Linux
permalink: /docs/how-to-locate-programs
---

## Command whereis

We use it to search binary files, as well as other commands, source and manual pages.

#### Example
{% highlight bash %}
whereis $1
{% endhighlight bash %}

Another option for whereis command ``` whereis -m```
We use it to search for manual page of some program.

#### Example
{% highlight bash %}
whereis -m $1
{% endhighlight bash %}

Another option for whereis command ```whereis -b```
We use it to search for binary files.

{% highlight bash %}
whereis -b $1
{% endhighlight bash %}
