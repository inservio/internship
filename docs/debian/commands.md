---
layout: default
title: Commands
parent: Debian
---

# Configure timezone

* Choose `Europe\Sarajevo`.

````
dpkg-reconfigure tzdata
````

Check if changes applied to `Europe\Sarajevo`.

````
cat /etc/timezone
````

Check date and time using command

````
date
````

Check again

````
dpkg-reconfigure -f noninteractive tzdata
````

# Configure locales

````
dpkg-reconfigure locales
````

use `en_US.UTF-8`

After check with command

````
dpkg-reconfigure locales --frontend noninteractive locales
````
