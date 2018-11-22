---
layout: single
title: Command Netstat
parent: Linux
permalink: /docs/linux/how-to-show-network-status/
---

{% include base_path %}


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


