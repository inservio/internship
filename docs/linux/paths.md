---
layout: default
title: Paths
parent: Linux
nav_order: 5
---

# Paths

## Introduction


### 2.3.3 Home folder

Korsnici imaju sopstveni `home` direktorij koji se nalazi u folderu `/home`. Izuzetak je `root` korisnik, čiji home direktorij se nalazi na lokaciji `/root`. U home direktoriji korisnici cuvaju svoje fajlove i personalne **login skripte** i **bash history** odnosno listu komandi koje su prethodno kucali.

* `~/.bashrc`
* `~/.bash_history`

Korisnik prilikom logovanja ce biti odveden u home direktorij. Putanja do home direktorija je definisana u varijabli `$HOME`. Mozemo ispisati trenutnu vrijednost **$HOME** varijable pomocu **echo** komande na sljedeci nacin.

````
echo $HOME
````
Korisnici mogu pristupiti home folderu tako sto koriste **cd** komandu bez argumenata te ako koriste znak tildu odnosno **~**.

#### Vježba: nekoliko načina kako pristupiti home folderu

* koristiti `cd` komanu bez argumenata.

```
cd
```

* kao argument `cd` komandi proslijediti znak tildu tj. `~`.

```
cd ~
```
* kao argument `cd` komandi proslijediti build in shell varijablu `$HOME`

```
cd $HOME
```

### 2.3.4 Prethodni direktorij

Korisna opcija komandi **cd** je **-** opcija. Njihova kombinacija izgleda ovako `cd -`. Ova komanda korisnika vraca u prethodni diretorij. Ovo funkcionise pomocu varijable **$OLDPWD**.

#### 2.3.4.1 Vjezba: vracanje u prethodni direktorij

````
cd ~
cd /tmp
echo $OLDPWD
cd $OLDPWD
cd /home
cd -
echo $OLDPWD
````

### 2.3.6 Putanje do Fajlova

Kada pristupamo fajlovimo koristimo putanje. Putanje mogu biti

* `apsolutne` putanje
* `relativne` putannje

Primjeri putanja

* **.** - Trenutni tj. tekući direktoriju.
* **..** - Direktorij iznad ili roditelj trenutnog direktorija.
* **../..** - Direktorij dva direktorija iznad trenutnog direktorija.
* **/etc/passwd** - Apsulutna ili puna putanja do fajla `passwd` koji se nalazu u sistemom `etc` direktoriju.
* **../etc/passwd** - Ukuloko je trenutni direktorij `/home` ovo bi bila relativna putanja na `passwd` fajla.
