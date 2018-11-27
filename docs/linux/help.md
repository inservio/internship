---
layout: default
title: Getting help
parent: Linux
nav_order: 5
toc: true
---


#### Using the Command Line to Get Help

Description: Running help commands and navigation of the various help systems.

**Key Knowledge Areas:**

*    Man
*    Info

**Terms and Utilities:**

*    man
*    info
*    Man pages
*    `/usr/share/doc/`
*    locate


### Opcija **-help**

```
ls —help
```

 -> pomoc o komandi


### Komanda *man*

Komanda ```man``` (manual) podrazumjeva nesto opsirniju dokumentaciju.
Riječ je o dokumentaciji koja opisuje naredbe, a koja je podijeljena na sekcije i stranice.
Sekcije/poglavlja pomazu odrediti kako se komande koriste npr. kao korisnik ili kao root korisnik

Ako želimo da nam se ispise stanica iz nekog konkretnog poglavlja, tada kao argument trebamo navesti broj poglavlja.

Sekcija 1 : Standardni korinik
Sekcija 5: Komanze konfiguracije fajla
Sekcija 8: Root korisnik



```man 1 komanda````


Koristenje komande ```whatis``` omogucava pronalazenje man stranica za datu komandu.

```whatis crontab```


```man ls```
-> man-om objasnjvamo komande i lista se sa f i b


Iz dokumentacije izlazimo sa ```q```


### Komanda *info*

Naredba info omogućava pristup do dokumenata koji čine drugi sistem pomoći, takozvane info-stranice. okumentaciju u ovom formatu imaju samo neki, većinom noviji programi posebno pisani upravo za Linux. Ukoliko ne postoji dokumentacija za traženi pojam među info-stranicama, naredba info će ispisati odgovarajuću man-stranicu (ako ona postoji).


```info komanda```
