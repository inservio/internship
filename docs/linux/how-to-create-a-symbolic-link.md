---
layout: default
title: How to create a link
parent: Linux
nav_order: 5
---

# How to a link

## Introduction

In order to create a link we ude the `ln` command. It is a standard Unix / Linux / BSD command to create links to files. There are two types of links:
* hard link,
* soft link.

## Demonstration

### Example for creating a symbolic link

{% highlight bash %}
touch slink
echo some_text > slink
ln -s slink some_text
cat slink
display output:
some_text
{% endhighlight bash %}

### Kreiranje simboličkih linkova

prvo napravimo fajl

```
touch fajl_jedan
```

zapišemo nesto u fajl pomoću redirekcije

```
echo "NEKI TESTNI SADRZAJ">fajl_jedan
```

provjerimo da li je zapisano u fajl

```
cat fajl_jedan
```

napravimo simbolički link na novi fajl

```
ln -s fajl_jedan fajl_dva_koji_je_simbolicki_link_na_prvi_fajl
```

ispišemo sadrzaj drugog fajla koji je simbolički link

```
cat fajl_dva_koji_je_simbolicki_link_na_prvi_fajl
```

možemo primjetiti da je sadržaj oba fajla isti

provjerimo inodove oba fajla

```
ls -i fajl_jedan
ls -i fajl_dva_koji_je_simbolicki_link_na_prvi_fajl
```

možemo promjetiti da su inode brojevi razliciti sto znaci da su razliciti fajlove te ako jedan izbrisemo to znaci da drugi fajl nece biti izbrisan
