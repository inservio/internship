---
layout: default
title: cd
parent: Commands
nav_order: 5
toc: true
---

## Introduction

### Getting help

````
cd -h
````

````
cd --help
````


#### Komanda **cd**

ulazak u folder

```
cd IME FOLDERA
```

SAMO `cd` vraca na pocetni folder odnosno home folder.


izlazak iz trenutnog foldera u jedan nivo vise.

```
cd ..
```

ulazak na udaljeni folder, dva levela iznad

```
cd ../../NEKI FOLDER
```

* Vise o komandi `cd`

````
man cd
````

#### ***Vjezba***

Pratiti kako se mijenja pwd vrijednost nakon svake izmjene current directorija

```
cd ~
pwd
echo $PWD
```

```
cd $HOME
pwd
echo $PWD
```
