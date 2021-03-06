---
layout: default
title: Let's Encrypt
parent: Zimbra
---

### Stop zimbra service

* Login as zimbra user and stop proxy and mailbox services.

````
su -l zimbra
zmproxyctl stop
zmmailboxdctl stop
````

or stop all zimbra services

````
zmcontrol stop
````

### Add your domain to list

* As user root

````
nano /root/certbot_komanda.sh
````

Check again if everything is ok.

````
cat /root/certbot_komanda.sh
````

### Run certificate generation

* As user root

````
sh /root/certbot_komanda.sh
````

###### Append to `chain.pem`

* As user root

Append Identrust X3 Root Certificate, the following key to `chain.pem`

````
-----BEGIN CERTIFICATE-----
MIIDSjCCAjKgAwIBAgIQRK+wgNajJ7qJMDmGLvhAazANBgkqhkiG9w0BAQUFADA/
MSQwIgYDVQQKExtEaWdpdGFsIFNpZ25hdHVyZSBUcnVzdCBDby4xFzAVBgNVBAMT
DkRTVCBSb290IENBIFgzMB4XDTAwMDkzMDIxMTIxOVoXDTIxMDkzMDE0MDExNVow
PzEkMCIGA1UEChMbRGlnaXRhbCBTaWduYXR1cmUgVHJ1c3QgQ28uMRcwFQYDVQQD
Ew5EU1QgUm9vdCBDQSBYMzCCASIwDQYJKoZIhvcNAQEBBQADggEPADCCAQoCggEB
AN+v6ZdQCINXtMxiZfaQguzH0yxrMMpb7NnDfcdAwRgUi+DoM3ZJKuM/IUmTrE4O
rz5Iy2Xu/NMhD2XSKtkyj4zl93ewEnu1lcCJo6m67XMuegwGMoOifooUMM0RoOEq
OLl5CjH9UL2AZd+3UWODyOKIYepLYYHsUmu5ouJLGiifSKOeDNoJjj4XLh7dIN9b
xiqKqy69cK3FCxolkHRyxXtqqzTWMIn/5WgTe1QLyNau7Fqckh49ZLOMxt+/yUFw
7BZy1SbsOFU5Q9D8/RhcQPGX69Wam40dutolucbY38EVAjqr2m7xPi71XAicPNaD
aeQQmxkqtilX4+U9m5/wAl0CAwEAAaNCMEAwDwYDVR0TAQH/BAUwAwEB/zAOBgNV
HQ8BAf8EBAMCAQYwHQYDVR0OBBYEFMSnsaR7LHH62+FLkHX/xBVghYkQMA0GCSqG
SIb3DQEBBQUAA4IBAQCjGiybFwBcqR7uKGY3Or+Dxz9LwwmglSBd49lZRNI+DT69
ikugdB/OEIKcdBodfpga3csTS7MgROSR6cz8faXbauX+5v3gTt23ADq1cEmv8uXr
AvHRAosZy5Q6XkjEGB5YGV8eAlrwDPGxrancWYaLbumR9YbK+rlmM6pZW87ipxZz
R8srzJmwN0jP41ZL9c8PDHIyh8bwRLtTcm1D9SZImlJnt1ir/md2cXjbDaJWFBM5
JDGFoqgCWjBH4d1QB7wCCZAA62RjYJsWvIjJEubSfZGL+T0yjWW06XyxV3bqxbYo
Ob8VZRzI9neWagqNdwvYkQsEjgfbKbYK7p2CNTUQ
-----END CERTIFICATE-----
````

Set permissions so zimbra user can read and write.

````
cd /etc/letsencrypt/live/YourServer.inservioserver.com
chmod 777 *
su zimbra
````

Check if necessary files exist in current directory.
````
ls -alh
````

You should have following files

````
cert.pem  chain.pem  fullchain.pem  privkey.pem
````

### Verify certificate

* Should be run as user zimbra

````
whoami
zmcertmgr verifycrt comm privkey.pem cert.pem chain.pem
````

You will should following output to screen.

```
** Verifying cert.pem against privkey.pem
Certificate (cert.pem) and private key (privkey.pem) match.
Valid Certificate: cert.pem: OK
```

It should say **Valid Certificate: cert.pem: OK**

### Deploy

Before deploying a good practice is to backup the old cert.

* as user zimbra

````
whoami
cp -a /opt/zimbra/ssl/zimbra /opt/zimbra/ssl/zimbra.$(date "+%Y%m%d")
````

Before deploying the SSL Certificate, you need to overwrite the existing `commercial.key` with `privkey.pem`.

````
yes | cp ./privkey.pem /opt/zimbra/ssl/zimbra/commercial/commercial.key
````

### Final deploy

* As user zimbra

````
su zimbra
zmcertmgr deploycrt comm cert.pem chain.pem
````

### Zimbra restart

* As user zimbra

````
su -l zimbra
zmcontrol restart
exit
````

## Links

https://wiki.zimbra.com/wiki/Installing_a_LetsEncrypt_SSL_Certificate
