---
layout: single
title:  "Introduction to the process information file system!"
date:   2018-08-25 13:31:20 +0200
categories: proc
---

# Overview of process information

The running process has a unique PID or Process ID, or a unique number that is recorded in the / proc directory.
The first boot process is the init process, and the number 1 is assigned as the first one.
If we want to see information about an init such as the status of the process, we are running the cat / proc / 1 / status command.
## Listi of command and examples

```cat /proc/1/status```

### Command free -m and command free -d

-Free -m we use when we want to see the free memory displayed in megabytes.
-Free -h we use when we want to see the free memory displayed in gigabytes.

### Command ```cat /proc/meminfo```

If we want to know the information about RAM memory we have to use command:

```cat /proc/meminfo```

### Command ```cat /proc/cpuinfo```

If we want to know the information about CPU (processor) we have to use command:

```cat /proc/cpuinfo```

### Command ```cat /proc/cmdline```
If we want to know which kernel is booting and with which parameters we have to use command:

```cat /proc/cmdline```

### Command ```cat /proc/partitions```

If we want to find the list of partitions we use command:

```cat /proc/partitions```

### Command ```cat /proc/version```
If we want to find out the kernel version we use command;
```cat /proc/version```

### Command ```cat /proc/uptime```
If we want to find out how long the system is running, we use command:
```cat /proc/uptime```
