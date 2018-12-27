---
layout: default
title: How to recover MySQL
parent: MySQL
---

# Put MySQL server in recovery mode

Edit `my.cnf` and under `[mysqld]` section Put

````
innodb_force_recovery = 1
````

Restart

check if systemd is used
````
systemctl list-unit-files | grep mysql
````

if not use init script to restart

````
/etc/init.d/mysql restart
````

If mysql service still does not start try increasing `innodb_force_recovery = 2` until `innodb_force_recovery = 6`.
