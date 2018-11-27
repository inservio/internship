---
layout: default
title: ps
parent: Commands
nav_order: 5
toc: true
---

## Introduction

### Getting help

````
````

#### Izlistaj sve procese svih korisnika

```
ps -ef
```
e --> ispis svih procesa u sistemu
f --> ispis dodatnih podataka o procesima


ili

```
ps -aux
```

### izlistaj procese samo za sshd korisnika

```
ps -f -u sshd
```

### sortiraj procese po potrošnji memorije

```
ps aux --sort pmem
```

### sortoranje procesa po CPU potrošnji

```
ps aux --sort pcpu
```
