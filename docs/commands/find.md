---
layout: default
title: find
parent: Commands
nav_order: 5
toc: true
---

## Introduction

find - search for files in a directory hierarchy


### Getting help

````
man find
find --help
````

## Komanda **find**

Sluzi za pretragu file-ova

```
find . -name “naziv”
find . -name “naziv*”
```

Rekurzivno pretrazi sve fajlove u odredisnom direktoriju (u sljedecom primjeru to je direktorij /home)

```
find /home
```

Pretraga za fajlovima, u tekucem direktoriju, samo tipa file (ne izlistavamo direktorije)

```
find . -type f
```

Pretraga za direktorijima, ne ispisuju se fajlovima

```
find . -type d
```

* Vise o komandi `find`

````
man find
````
