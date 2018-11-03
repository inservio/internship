---
layout: post
title:  "Domain Name System!"
date:   2018-10-4 13:31:20 +0200
categories: dns
---
# Domain Name System (DNS)
## What is DNS?

The Domain Name System (DNS) is the phonebook of the Internet.
Web browsers interact through Internet Protocol (IP) addresses.
DNS translates domain names to IP addresses so we don't have to remeber IP address for example of google.com (172.217.16.206).
### Examples for DNS
### www.google.com. (172.217.16.206)
##### Root - .
##### TLD - top level domain in this case is com.
##### Domain name - google
##### Subdomain -www.
##### FQDN- fully qualified domain name in this case is www.google.com

## List of DNS record types

The list of DNS record types is an overview of resource records (RRs) permissible in zone files of the Domain Name System (DNS).

### Resource records:

    A (Address record) - Returns a 32 bit IPv4 address, most commonly used to map hostnames to an IP address of the host.

    AAAA (IPv6 address record) - Returns a 128-bit IPv6 address, most commonly used to map hostnames to an IP address of the host.

    MX (Mail exchange record) - Maps a domain name to a list of message transfer agents for that domain.

    NS (Name server record) - Delegates a DNS zone to use the given authoritative name servers.

    TXT (Text record) - If we want to set the human-readable text in DNS record.


### The command dig is a tool for querying DNS name servers.

#### Dig will let us perform any valid DNS query, the most common of which are:

    A (the IP address)
    TXT (text annotations)
    MX (mail exchanges)
    NS name servers


### Examples

If we want to display A records use the command dig A.

```dig google.com A```

### Display the output

{% highlight bash %}
;; QUESTION SECTION:
;google.com.                    IN      A

;; ANSWER SECTION:
google.com.             6       IN      A       172.217.16.110
{% endhighlight bash %}

### Another option is 
{% highlight bash %}
dig A google.com +short
{% endhighlight bash %}

### Display the output

```172.217.16.110```

If we want to display MX records use the command dig MX.

```dig google.com MX```

### Display the output

{% highlight bash %}
;; QUESTION SECTION:
;google.com.                    IN      MX

;; ANSWER SECTION:
google.com.             487     IN      MX      50 alt4.aspmx.l.google.com.
google.com.             487     IN      MX      40 alt3.aspmx.l.google.com.
google.com.             487     IN      MX      20 alt1.aspmx.l.google.com.
google.com.             487     IN      MX      30 alt2.aspmx.l.google.com.
google.com.             487     IN      MX      10 aspmx.l.google.com.
{% endhighlight bash %}

### Another option is 
{% highlight bash %}
 dig MX google.com +short
{% endhighlight bash %}

### Display the output

{% highlight bash %}
50 alt4.aspmx.l.google.com.
30 alt2.aspmx.l.google.com.
20 alt1.aspmx.l.google.com.
40 alt3.aspmx.l.google.com.
10 aspmx.l.google.com.
{% endhighlight bash %}

If we want to display NS records we use the command dig NS.

```dig google.com NS```

### Display the output

{% highlight bash %}
;; QUESTION SECTION:
;google.com.                    IN      NS

;; ANSWER SECTION:
google.com.             150015  IN      NS      ns3.google.com.
google.com.             150015  IN      NS      ns1.google.com.
google.com.             150015  IN      NS      ns2.google.com.
google.com.             150015  IN      NS      ns4.google.com.
{% endhighlight bash %}

### Another option is: 
{% highlight bash %}
dig NS google.com +short
{% endhighlight bash %}

### Display the output

{% highlight bash %}
ns4.google.com.
ns1.google.com.
ns2.google.com.
ns3.google.com.
{% endhighlight bash %}

If we want to display TXT records we use the command 
{% highlight bash %}
dig TXT google.com
{% endhighlight bash %}

### Another option is
{% highlight bash %}
dig TXT google.com +short
{% endhighlight bash %}

If we want to display CNAME records we use the command
{% highlight bash %}
dig CNAME google.com
{% endhighlight bash %}

### Another option is
{% highlight bash %}
dig CNAME google.com +short
{% endhighlight bash %}

If we want to explicitly dig nameserver NS we use the command
{% highlight bash %}
dig @ns1.google.com. google.com A
{% endhighlight bash %}

### Another option is
{% highlight bash %}
dig @ns1.google.com. google.com A +short
{% endhighlight bash %}
