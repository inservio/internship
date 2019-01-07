---
layout: default
title: Recover
parent: Zimbra
---

## How to manually recover email messages


#### Find compressed messages

````
find /opt/zimbra/store/ | xargs zgrep -m1 -l '<fristname.lastname@domain.tld>' > messages.gzip.list
````

### Create message list

** Import `Cc` **

````
grep -rl -E -m1 'Cc.*fristname\.lastname' /opt/zimbra/store/ > messages_to_recover.list
````

** Import `From` **


````
grep -rl -E -m1 'From.*fristname\.lastname' /opt/zimbra/store/ >> messages_to_recover.list
````

** Import `To` **


````
grep -rl -E -m1 'To.*fristname\.lastname' /opt/zimbra/store/ >> messages_to_recover.list
````



### Filter only `unique` messages

````
cat messages_to_recover.list | sort | uniq -u > messages_to_recover.unique.list
````


### Start import of messages

* Login to user account and create folder `Recovery`


* Execute bash script to import messages

````
#!/bin/sh
for i in `cat messages_to_recover.unique.list`
do
  /opt/zimbra/bin/zmmailbox -z -m fristname.lastname@domain.tld addMessage /Recovery $i
done
````
