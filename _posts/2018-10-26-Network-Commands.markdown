---
layout: post
title:  "Network Commands!"
date:   2018-10-4 13:31:20 +0200
categories: Network Commands
---

## Command ```nslookup```
We use when we want to check validity of the host name.

### Example
{% highlight bash %}
nslookup google.com
{% endhighlight bash %}

## Command ```ping```
Using a ping command, we check whether a host is working.
The Ping command sends a special message type, called Internet control echo request message, or an ICMP echo request (ICMP is an Internet control message protocol). 
This message asks the remote computer to return the echo reply, as a duplicate echo request message.
A low-level networking software running on a remote computer responds to an echo request so that the machine should be able to respond to the ping if its network software is running.

### Example
{% highlight bash %}
ping google.com
{% endhighlight bash %}

