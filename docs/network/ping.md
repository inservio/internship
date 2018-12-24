---
layout: default
title: ping
parent: Network
---

# Introduction command ping

Using a ping command, we check whether a host is working.
The Ping command sends a special message type, called Internet control echo request message, or an ICMP echo request (ICMP is an Internet control message protocol).
This message asks the remote computer to return the echo reply, as a duplicate echo request message.
A low-level networking software running on a remote computer responds to an echo request so that the machine should be able to respond to the ping if its network software is runnin$

## Demonstration

### Example
{% highlight bash %}
ping google.com
{% endhighlight bash %}

#### More examples for ping command

##### Command ```ping -i```
we use to specify how much time will it take for ping command to execute.
{% highlight bash %}
ping -i 3 google.com
{% endhighlight bash %}

##### Command ```ping -c```
we use to specify the execute number for ping command.
{% highlight bash %}
ping -c 5 google.com
{% endhighlight bash %}

##### Command ```ping -s 100 google.com```
we use when we want to change the size of the packet.

{% highlight bash %}
ping -s 100 google.com
{% endhighlight bash %}
