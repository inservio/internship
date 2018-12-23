---
layout: default
title: Zimbra Commands
parent: Zimbra
---

## How to create domain

### Demonstration

```
zmprov cd domain.com zimbraAuthMech zimbra
```
## Creating account and modify

* We first need do generate random password
* Run the command

````
RANDOM_PASSWORD=$(head -c 222 /dev/urandom | md5sum| base64)
````

* Display the generated password

````
echo $RANDOM_PASSWORD
````

### Create account

* Run the command and use random generated password

````
zmprov ca account@domain.com $RANDOM_PASSWORD
````

* Test check with webmail

### Modify account

* How to change user's password

````
zmprov ma email@domain.com UserPassword $RANDOM_PASSWORD
````

* Again test with webmail




## Get All Domains

Check if the domain is on the list.

````
zmprov -l gad
````
