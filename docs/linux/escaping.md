---
layout: default
title: Escaping
parent: Linux
nav_order: 5
toc: true
---

### “Escaping” characters

Ako zelimo napraviti fajl sa razmakom u imenu, moramo koristiti navodnike. Koristenje navodnika je jedan vid tzv. “Escaping” karaktera.  “Escaping” je potrebno raditi sa svim specijalnom karakterima.

Pored razmaka u specijalne karaktere ubrajamo

````
$&;(){}[]*?!<>"'
````

* Za “Escaping” samo jednog karaktera koristimo znak `\` ili backslash.
* Za “Escaping” vise rijeci od jednom koristimo jednostruke `''` i dvostruke `"…"` navodnike.

#### Pravljenje fajla sa razmakom u imenu

````
touch 'Novi Fajl'
````

Kada ne bi koristili navodnike

````
touch Novi Fajl
````

napravili bi smo dva fajla i to `Novi` i `Fajl`.

#### Fajlovi i direktoriji koji imaju razmak u imenu

File ili direktorij sa space Moj File se pise kao ```Moj\ file```
