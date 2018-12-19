---
layout: default
title: How to performe valid DNS query with dig
parent: DNS
permalink: /docs/dns/dig/
---
# Examples for dig command

#### Query Address record with dig command
If we want to display A records use the command dig A.

```
dig google.com A
```

#### Another option is
{% highlight bash %}
dig A google.com +short
{% endhighlight bash %}


#### Query Mail exchange record with dig command

If we want to display MX records use the command dig MX.

```
dig google.com MX
```

#### Another option is
{% highlight bash %}
dig MX google.com +short
{% endhighlight bash %}

#### Query Name server record with command dig
If we want to display NS records we use the command dig NS.

```dig google.com NS```

#### Another option is:
{% highlight bash %}
dig NS google.com +short
{% endhighlight bash %}

#### Query Text record with command dig
If we want to display TXT records we use the command
{% highlight bash %}

dig TXT google.com
{% endhighlight bash %}

#### Another option is
{% highlight bash %}
dig TXT google.com +short
{% endhighlight bash %}

#### Query Canonical name record with command dig
If we want to display CNAME records we use the command
{% highlight bash %}
dig CNAME google.com
{% endhighlight bash %}

#### Another option is
{% highlight bash %}
dig CNAME google.com +short
{% endhighlight bash %}

#### Query explicitly Name server record with command dig
If we want to explicitly dig nameserver NS we use the command
{% highlight bash %}
dig @ns1.google.com. google.com A
{% endhighlight bash %}

#### Another option is
{% highlight bash %}
dig @ns1.google.com. google.com A +short
{% endhighlight bash %}

#### Query SPF Sender Policy Framework
SPF is an alternative to storing SPF data in TXT records, using the same format. 
{% highlight bash %}
dig google.com TXT +short
{% endhighlight bash %}
