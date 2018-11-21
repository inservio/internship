---
layout: single
title: Command uniq
parent: Linux
permalink: /docs/linux/how-to-report-or-filter-out-repeated-lines-in-a-file/
---

{% include base_path %}


## Command ```uniq```
We use when we want to eliminate duplicate adjacent rows from a file, or from a standard input, in order to generate a standard output, or another file.

#### Example
{% highlight bash %}
uniq $1
{% endhighlight bash %}

Another option for uniq command ```uniq -u```
We use when we want to display rows that appear only once in the file.

#### Example
{% highlight bash %}
uniq -u $1
{% endhighlight bash %}

Another option for uniq command ```uniq -f```
We use when we want to skip rows.

{% highlight bash %}
uniq -f $1
{% endhighlight bash %}

Another option for uniq command ```uniq -d```
We use when we want to display only duplicate rows.

{% highlight bash %}
uniq -d $1
{% endhighlight bash %}
