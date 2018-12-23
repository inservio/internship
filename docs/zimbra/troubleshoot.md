---
layout: default
title: Troubleshooting
parent: Zimbra
---

## How to track messages sent and received by a user

### Demonstration

```
/opt/zimbra/libexec/zmmsgtrace -s user@example.com
```


## Change Zimbra DNS resolve to native

````
su zimbra -l
postconf | grep host_lookup
postconf -e lmtp_host_lookup=native
````
