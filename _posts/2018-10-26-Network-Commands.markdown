---
layout: post
title:  "Network Commands!"
date:   2018-10-4 13:31:20 +0200
categories: test category
---

## Command ```nslookup```
We use when we want to query Internet domain name servers. 

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

## Command ```traceroute```
We use it to show details about the path that a packet takes to a specified destination.
### Exaample 
{% highlight bash %}
traceroute google.com
{% endhighlight bash %}

## Command ```host```
We use it when we want to display the hostname from IP address.
{% highlight bash %}
host 172.217.20.14 
{% endhighlight bash %}

#### More examples for hostname 

Hostname -d - displays the domain name that machine belongs to.
Hostname -f - displays the fully qualified host and domain name.
Hostname -i - displays the IP address for the current machine.


#### Examples for ifconfig

```ifconfig -a```  View all network configuration and settings.
```ifconfig eth0```  View specific network settings.
```ifconfig eth0 up or ifup eth0```  Enabling eth0 interface.
```ifconfig eth0 down or ifdown eth0``` Disabling eth0 interface.


## NAT 
is used in routers NAT translates a set of IP addresses to another set of IP addresses.
NAT helps preserve the limited amount of IPv4 public IP addresses.

## Netstat
Most useful and very versatile for finding connection to and from the host.

#### Examples for netstat command

```netstat -a or netstat -all```
Display all connections including TCP and UDP.

```netstat --tcp or netstat -t```
Display only TCP connection.

```netstat -u or netstat --udp```
Display only UDP connection.

```netstat -g```
Display all multicast network subscribed by this host.

```netstat -l```
List only listening ports.
