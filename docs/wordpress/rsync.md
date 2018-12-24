---
layout: default
title: RSYNC      
parent: Wordpress
---

# Howto sync directories with RSYNC

* Install `rsync` package on both hosts, source and remote.

````
apt-get install rsync
````

## Sync

In this example we will sync local `/var/www/blatusa.com` directory to remote server with hostname `server.com`.

````
rsync -avz -e 'ssh -p 22' /var/www/blatusa.com/ root@server.com:/var/www/blatusa.com/
````