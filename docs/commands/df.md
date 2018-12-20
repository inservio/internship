---
layout: default
title: df
parent: Commands
nav_order: 5
toc: true
---

## Introduction

`df` - report file system disk space usage


### Getting help

````
df --help
man df
````

### Command ```df```

we use when we want to get the attributes of all, or the specified file systems on the operating system.

#### Display disk usage in MB

```
df -m
```

we use when we want to display free memory on hard disk in megabytes

#### Display disk usage in human-readable format

````
df -h
````

or
````
df --human-readable
````

#### Display disk usage and file system type

```
df -hT /home
```

in this example we use the command when we want to display disk usage of `/home` partition.

#### Display inode usage on partition

In this example we will display the inode disk usage on the root partition.

````
df -hi /
````
