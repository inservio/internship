---
layout: default
title: Hidden files
parent: Linux
nav_order: 5
toc: true
---

# Introduction

Skriveni fajlovi

U Linuxu skriveni fajlovi su fajlovi cije ime pocinje sa **tackom** odnosno znakom **.**. Da bi izlistali skrivene fajlove koristimo opciju **-a** sa komandom **ls** da nam izlista sve vrste fajlova ukljucujuci i skrivene fajove.

Pomocu pipinga i grep komande mozemo izlistati sve fajlove koji pocinju sa znakom **.**.

## Demonstration

````
ls -a | grep '^.'
````

Komanda **ls** ima opcije **-a** i **-A**.

* opcija **-a** izlistava sve fajlove
* opcija **-A** islistava skoro sve

Opcija **-A** ne izlistava trenutni direktorij cija je oznaka sama **tacka** odnosno znak **.** te ne izlistava direktorij roditelj cija je oznaka **dvije tacke** odnosno **..**.
