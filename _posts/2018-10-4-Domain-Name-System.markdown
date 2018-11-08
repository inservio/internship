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
#### Query Address record with dig command 
If we want to display A records use the command dig A.

```dig google.com A```

#### Another option is 
{% highlight bash %}
dig A google.com +short
{% endhighlight bash %}


#### Query Mail exchange record with dig command 
If we want to display MX records use the command dig MX.

```dig google.com MX```

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
