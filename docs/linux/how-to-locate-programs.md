---
layout: default
title:  Command whereis
parent: Linux
nav_order: 5
toc: true
---


## Command whereis

We use it to search binary files, as well as other commands, source and manual pages.

#### Example
{% highlight bash %}
whereis $1
{% endhighlight bash %}

Another option for whereis command ``` whereis -m```
We use it to search for manual page of some program.

#### Example
{% highlight bash %}
whereis -m $1
{% endhighlight bash %}

Another option for whereis command ```whereis -b```
We use it to search for binary files.

{% highlight bash %}
whereis -b $1
{% endhighlight bash %}


### Pronalazenje putanje do programa pomocu komandi `whereis` i `which`


Koristimo komandu whereis i which da saznamo putanju gdje je instaliran program, odnosno gdje se nalazi binary trazenog programa

#### Komanda **which**

Komanda sluzi za pronalazenje datoteka u korisnickim putanja. Komanda provjerava da li fajl postoji u korisnickoj `$PATH` varijabli.

```
which nano
```

Ako se komanda ne nalazi u putanjama unutar `$PATH` varijable, komanda vraca prazan rezultat.

* Primjer

Logujemo se kao neprivilegovani korisnik

````
su -l korinsnik
````

````
which ifconfig
````

Dobijamo prazan odgovor.

* Vise o komandi `which`

````
man which
````


#### Komanda **whereis**

komanda sluzi za pretragu za `binary` datotekama odnosno ostalim komandama, source i manual stranica.

* Primjeri upotrebe

```
whereis nano
```

```
whereis bash
```


* Pretraga gdje se nalazi **binarna** datoteka

````
whereis -b bash
````

* Pretraga za **manual** stranicama nekog programa

````
whereis -m bash
````

* Vise o komandi `whereis`

````
man whereis
whereis --help
````
