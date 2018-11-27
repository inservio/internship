---
layout: default
title: ls
parent: Commands
nav_order: 5
toc: true
---

## Introduction

 ls - list directory contents


### Getting help

````
man ls
````

### 2.3.7 Ispis sadržaja direktorija sa komandom `ls`

Listanje

```
ls
```

Listaj **a**-detalje, **l**-long format, **h**-velicina fileova izrazena razumljivije

```
ls —a -l -h
```

ili ovako:

```
ls -alh
```

##### Ispisi listu fajlova i direktorija unutar trenutnog direktorija

Ako zelimo izlistati sadrzaj tekuceg foldera korisimo komandu ispod.

```
ls .
```

* Ispisi listu fajlova i direktorija unutar trenutnog direktorija ukljucujuci i sakrivene fajlove skriveni fajlvi su fajlovi cije ime pocinje sa tackom odnosno znakom .

```
ls -al .
```

* Ispisi listu fajlova i direktorija unutar trenutnog direktorija, te sadrzaj direktorija koji se nalaze u tekućem direktoriju

```
ls -al *
```

* Ispisi listu fajlova i direktorija unutar trenutnog direktorija na nacin da i direktorije tretiramo kao obične fajlove te ne ispisujemo njihov sadržaja

```
ls -ald *
```

Ispisi listu fajlova i direktorija koji pocinju sa znakom `.` odnosno ispisi samo skrivene fajlove i direktorije

```
ls -ald .*
```


#### Ispisi inode broj fajla

```
ls -i ime_fajla
```

Gledanje u sadrzinu i oko foldera rekurzivno tj. pregled cijele strukture foldera

```
ls -R IME FOLDERA/
```
