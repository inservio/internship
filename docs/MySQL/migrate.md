---
layout: default
title: How to migrate MySQL
parent: MySQL
---

# Migrate all databases

Put MySQL server in read only mode.

* edit `my.conf` and under

````
read-only=1
````

restart MySQL

* Backup all databases

````
mysqldump -u root -p --all-databases>all.sql
````
