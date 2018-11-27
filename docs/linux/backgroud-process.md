---
layout: default
title:  Entering the commands that are processed in the background
parent: Linux
nav_order: 5
toc: true
---


## Entering the commands that are processed in the background

Shell provides the ability to handle commands in the background.
This is achieved by setting the ampersand symbol, &, to the end of the command.

{% highlight bash %}
find / -name "$1" -print > find.results 2>/dev/null &
{% endhighlight bash %}


### Slanje procesa i background

Da bi poslali komandu u backgroun, nakon komande dodamo znak `&` tj. znak ampersand.

U sljedecem primjeru zelimo da pingamo google svakih 5 sekundi sa komandom `ping -i 5 google.com`. Da bi je poslali u background, aa sami kraj komande dodajemo znak `&`.

```
ping -i 5 google.com &
```

Na ovaj nacin komanda ce biti izvrsavana u pozadini i svakih 5 sekundi ce nam ispisati rezultat na ekran, dok se rad u terminalu moze nastaviti.



* izlistamo procese u backgroundu

```
jobs
```

vratimo komandu u foreground

```
fg
```

```
jobs
[1]+  Running   "Komanda koju smo poslali u background"
```
Procesi su programi koji se izvršavaju. Programi su izvršene datoteke.
Prilikom pokretanja sistem svakom procesu dodjeljuje njegov broj (PID). Taj je broj jedinstven.


##### Procesima se mogu slati različiti signali, različitih značenja. Neki od signala su:

SIGHUP (1) - zahtjev za re-inicijalizacijom procesa
SIGKILL (9) - zahtjev za grubim prekidom izvršavanja
SIGTERM (15) - zahtjev za prekidom izvršavanja (softverski završetak rada)

Sintaksa:

```
kill [-s SIGNAL] PROCES
```


Naredbi ```kill``` se kao argument treba zadati PID procesa čije izvođenje želimo prekinuti ili redni broj koji je procesu dodijelila ljuska. Ako se navodi redni broj koji je procesu dodijelila ljuska tada ispred njega treba upisati znak % .

Ako se ne navede signal koji šaljemo, podrazumijeva se da se radi o signalu SIGTERM. Signale možemo zadati njihovim rednim brojem ili simboličkim imenom.

```
$ kill -9 12345
```
 —>program prekidamo navodeći njegov PID

```
$ kill-9 %2
```
 —> Program prekidamo dodjeljivanjem rednog broja bash-a

```
kill 1 --> broj procesa
```


#### Zapisivanje poruka u log datoteku

U proslom primjeru samo koristi komandu koja pinga `google.com` svakih 5 sekundi te nam ispisuje rezultate na `STDOUT` odnosno ekran. To je u odredjenim situacijama korisno jer korisnika informise u statusu izvrsavanja komande u pozadini, ali cesto samo ometa korisnika u radu.

U situacijama gdje ne zelimo da komanda ispisuje nepotrebne informacije na ekran koristimo redirekciju u fajl pomocu znaka `>`. To mozemo uraditi na sljedeci nacin.

* U ovom primjeru pingamo `google.com` svakih `5` sekundi te poruka koje salje komanda redirektujemo sa ekrana u fajl `/tmp/ping_google.log`, te na samom kraju stavljamo znak `&` cime zeljenu komandu saljemo u background.

````
ping -i 5 google.com > /tmp/ping_google.log &
````

Sada mozemo nastaviti sa radom a ako zelimo periodicno provjeriti stanje komande koristimo `tail` da bi procitali zapis u fajl `/tmp/ping_google.log`.

````
tail /tmp/ping_google.log
````

ili citanja u `real time` modu

````
tail -f /tmp/ping_google.log
````

Ako zelimo prekinuti `real time` citanje koristimo kombinaciju tipki `CTRL+C`.
