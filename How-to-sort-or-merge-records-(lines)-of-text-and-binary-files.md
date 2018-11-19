---
layout: default
title: Command sort
parent: Advanced Commands
nav_order: 6
---

## Commands ```sort```
We use when we want to sort the specified file according to the specified order.

#### Example
{% highlight bash %}
sort $1
{% endhighlight bash %}

Another option for sort command ```sort -u```
We use when we want to keep only one row, in the case when the result of sorting appears more same rows.

#### Example

{% highlight bash %}
sort -u $1
{% endhighlight %}

Another option for sort command ```sort -r```
We use if we want to sort the file in reverse order.

#### Example
{% highlight bash %}
sort -r
{% endhighlight bash %}

Another option for sort command ```sort -f```
We use when we want to sort the file in the order of capital letters.

#### Example
{% highlight bash %}
sort -f
{% endhighlight bash %}

Another option for sort command ```sort -d```
We use it if we want to sort the file in alphabetical order.

#### Example
{% highlight bash %}
sort -d
{% endhighlight bash %}
