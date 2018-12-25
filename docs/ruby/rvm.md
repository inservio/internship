---
layout: default
title: RVM
parent: Ruby
---

## Autoupdate RVM

````
\curl -sSL https://get.rvm.io | bash -s stable
````

````
echo rvm_autoupdate_flag=2 >> ~/.rvmrc
````

# Import key

Add

````
deb http://ftp.de.debian.org/debian stretch-backports main
````

to

````
/etc/apt/sources.list
````

run update

````
apt-get update
````

install

````
apt-get install gnupg2 -t stretch-backports
````
