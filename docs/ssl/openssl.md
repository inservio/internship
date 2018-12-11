---
layout: default
title: Openssl      
parent: SSL
---

# How to generate a CSR

CSR openssl configuration contains by default the details as follows below:

    Common Name (the domain name certificate should be issued for)
    Country (two-letter code)
    State (or province)
    Locality (or city)
    Organization
    Organizational Unit (Department)
    E-mail address


To generate a CSR run the command below in terminal:

````
openssl req -new -newkey rsa:2048 -nodes -keyout domain.key -out domain.csr
````

# Merge bundle and certificate

````
cat domain_com.crt <(echo) domain_com.ca-bundle >domain_com_bundle.crt
````
