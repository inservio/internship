---
layout: default
title: Troubleshoot
parent: DNS
permalink: /docs/dns/troubleshoot/
---

## How to override in /etc/hosts

In this demonstration I am going to show how to use the /etc/hosts file to locally point a domain to another IP.
I am using example.com ip address as an example.

````
93.184.216.34
````
To add this ip address we will first need to edit hosts file with nano editor.

````
nano /etc/hosts
````

### In hosts file

````
 Host Database

 localhost is used to configure the loopback interface
 when the system is booting.  Do not change this entry.

 93.184.216.34 example.com

````

### Chack the domain

````
ping -c 1 example.com
PING example.com (93.184.216.34): 56 data bytes
64 bytes from 93.184.216.34: icmp_seq=0 ttl=55 time=138.478 ms
````
