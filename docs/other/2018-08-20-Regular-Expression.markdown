---
layout: default
title:  "Regular Expression"
date:   2018-10-4 13:31:20 +0200
parent: Other
---


## Interval Regular expressions

### Example
---

{% highlight bash %}

cat README.md | grep l

{% endhighlight bash %}


## Brace expansion


{% highlight bash %}
echo Aa Bb Cc Dd
echo {0..100}
echo a{0..10}b

{% endhighlight bash %}

## Basic Reuglar expressiond

### Example
```^``` we use for search for the beginning string.
```$``` we use for search for the end of the string.

#### More examples
{% highlight bash %}

cat README.md | grep '^L'

cat README.md | grep 'A$'

{% endhighlight bash %}
