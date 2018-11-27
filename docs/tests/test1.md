---
layout: default
title: Test1
parent: Tests
permalink: /docs/tests/test1/
---

{:toc}

# Pitanja



2. Sta je znaci akronim odnosno komanda ````ls````?



3. Sta je znaci akronim odnosno komanda ````pwd````?



11. Opisati komandu ````id -G root````



12. Opisati komandu ````which ls````



13. Opisati komandu `ls -a | grep '^.'`



14. Koji ````numericki ID```` je dodijeljen korisniku ````root````?



15. Opisati komandu `ls .`




16. Opisati komandu `ls * `



17. Opisati komandu ````chmod -x cat.sh````



18. Opisati komandu ````ls -i /etc/passwd````



19. Opisati komandu ````ECHO $OLDPWD````


20. Opisati komandu ````find . -type f````


21. Sta predstavlja ````$OLDPWD```` u komadi ````ECHO $OLDPWD````?



22. Opisati komandu ````./cat.sh````




23. Koja je rezlika izmjedju komandi ````id -g root```` i ````id -G root````?



24. Gdje se nalazi sljedeca fatoteka ````~/.bashrc```` ?




25. Kojom komandom proveravamo koji je ````SHELL```` podesen za trenutnog korisnika?



30. Opisati komandu ````find . -type d````



31. Opisati komandu ````man find````



32. Opisati komandu ````whereis -b bash````



33. Opisati komandu ````whereis -m bash````




35. Sta ce biti rezultat komande ````id -g root````?



36. Opisati komandu ````su korisnik -l````



37. Opisati komandu ````cp -p kakoje.rb kakoje2.rb````



38. Sta predstavlja ````#!/bin/bash````



39. Na kojoj liniji unutar fajla se nalazi ````#!/bin/bash````?



40. Kako se popularno nazivaju znakovi ````#!```` u sljedecem primjeru ````#!/bin/bash```` ?



41. Opisati komandu ````chmod +x cat.sh````.



47. Sta je u primjeru ````ls -l /etc/passwd```` argument, sta je komanda, a sta je opcija?



48. Za sta sluzi komnda ````type````?



49. Sta postize komanda ````touch 'kakoje'````?


50. Zasto koristimo jednostruke navodnike u komandu ````touch 'kako je'````



52. Zasto dobijamo sljedecu gresku?
```
$ ./cat.sh
-bash: ./cat.sh: Permission denied
```  


53. Opisati komandu ````#!/usr/bin/env ruby````.


54. Opisati komandu ````grep root /etc/passwd | head -n 1````


55. Sta ce biti rezultat komande ````id -u root```` ?


58. Opisati komandu ````who````






60. Opisati komandu ````printenv````




61. Opisati komandu ````echo $USER````



62. Opisati svaki korak sljedeceg primjera. Koji je rezultat posljednje komande?
````
touch osoba
echo ime_prezime > osoba
ln -s osoba ime_prezime
cat ime_prezime
````






63. Opisati komandu ````cp $1 $2````





64. Opisati komandu ````df -h````





65. Opisati komandu ````printenv | grep HOME````








75. Kako se zove specijalni znak ````|```` u komandi ````ls | sort````




76. Opisati komandu ````ls | sort -n````




77. Koji je razultat komande ````ls . > ls````?







87. Sta predstavlja specijalno znak ````&```` u komandi ````find /tmp -name "cao" -print > find.results 2>/dev/null &```` ?




88. Sta ce biti rezultat komande ````head -c 1 /dev/urandom```` ? Objasniti.




89. Sta ce biti rezultat komande ````echo "PING" >/dev/null```` ? Objasniti.



90. Sta predstavlja specijalni znak ````;```` u komandi `ls ; ps ; cd ; ls` ?



91. Koje informacije dobijamo sa komandom ````cat /proc/meminfo```` ?



92. Koje informacije dobijamo sa komandom ````cat /proc/meminfo | grep 'MemFree\|MemTotal'```` ?



93. Kako saznati listu particija na Linux sistemu?



94. Koje informacije dobijamo sa komandom ````cat /proc/cpuinfo```` ?



95. Koje informacije dobijamo sa komandom ````cat /proc/version```` ?



96. Koje informacije dobijamo sa komandom ````cat /proc/uptime```` ?



97. Koja komanda vrijednosti iz pseudo datoteke ````cat /proc/uptime```` prikazuje u human readable formatu?



98. Koja komanda zamijenjuje komandu ````cat /proc/version```` ?



99. Koje informacije dobijamo komandom ````cat /proc/cmdline````?



100. Kako se zove proces sa ````PID-om```` ````1````?



101. Sta nam prikazuje sljedeca komanda ````cat /proc/1/status | grep 'Name'````?



102. Sta je funkcija komande ````shutdown -r now````?






104. Sta je ````GRUB````?



105. Sta je ````SWAP```` particija?



106. Kako saznati Debian verziju?



107. Potrebno je koristiti output komandu ````ls```` kako bi se prepisao sadrzaj fajla ````bazz````. Koju od ponudjenih komandi bi koristili.  
  A. ````ls > bazz````  
  B. ````ls >& bazz````  
  C. ````ls &> bazz````  
  D. ````ls >> bazz````  


108. Editujete text dokument u ````vi```` editoru. Potrebnoje snimiti izmjene i napustiti edutor. Koje DVIJE ulazne sekvence ce postici zeljeni rezultat? Zaokruziti.  
  A. ````esc ZZ````  
  B. ````ctrl :w!````
  C. ````esc zz````  
  D. ````esc :wq!````
  E. ````ctrl XX````  



109. Koju komandu koristimo da bi process ostao u running stanju i nakon sto se korisnik odluguje?  
   A. live  
   B. nohup  
   C. saferun  
   D. sh  










122. Opisati komandu ````lsblk````

123. Opisati komandu ````fdisk -l````

124. Koja ja namjena komande ````mkfs.ext4````

125. Opisati komandu ````mount /dev/sdc /mnt/sdc/````


127. Opisati komandu ````blkid````

128. Razlika izmedju komande ````apt-get update```` i ````apt-get upgrade````

129. Cemu sluzi komanda ````dpkg-reconfigure tzdata````

130. Sta ispisuje komanda ````date````?

131. Za sta sluzi komanda ````git clone```` ?


133. Opisati komandu ````cat /home/rails/.ssh/id_rsa.pub````

134. Sta radi komanda ````curl 'http://google.com:80/fajl.pdf' > fajl.pdf```` te preko kojeg protokola i porta?

135. Zbog cega koristimo ````sudo```` komandu?


138. Koja je razlika izmedju komandu ````grep root /etc -r```` i ````grep root /etc -rl````?

139. Koji je fault tolerance za ````RAID0````?

140. Koji je fault tolerance za ````RAID1````?

141. Koji je fault tolerance za ````RAID5````?

142. Koji je fault tolerance za ````RAID6````?

143. Koji je fault tolerance za ````RAID10````?

144. Koji RAID ima bolje performance ````RAID5```` ili ````RAID10````?

145. Sta je ````Varnish````?

146. Da li ````NginX```` loadira module na ````staticki```` ili ````dinamicki```` nacin?

147. Koje permisije na fajl postavlja komanda ````chmod 777 /tmp/staima````

148. Koje persmije ima grupa,vlasnik i ostali u ovom slucaju ````-rwxrwxrwx````

149. Nakon ````chown root.root /tmp/backup.sh```` izvrsene komande koji korisnik te koja grupa je valsnik fajla?

150. Koji je rezultat sljedece komande ````chmod o-w /tmp/backup.sh````



152. Koja je razlika izmedju komande ````hostname```` i ````hostname -f````

153. Koji ````SHELL```` koristi korisnik u sljedecem primjeru?

````
nobody:*:-2:-2:Unprivileged User:/var/empty:/usr/bin/false
````


154. Koji direktorij je postavljen za home u sljedecem primjeru te za kojeg korisnika?

````
mail:x:8:8:mail:/var/mail:/usr/sbin/nologin
````

155. Na kojem mjestu u sljedecem primjeru bi se trebao nalaziti password?

````
web138:x:5006:5007::/var/www/clients/client110/web138:/bin/false
````

156. Zbog cega izvrasavamo komandu ````echo $PATH````?


157. Zbog cega se koristi komanda ````find /tmp/ | wc -l````?

158. Sta znace skracenice ````STDIN````, ````STDOUT```` i ````STDERR````

159. Sta se nalazi u direktorijumu ````/dev````?



161. Koja je razlika izmjedu ````head```` i ````tail```` komandi?


162. Komandu ````ls ~/..```` napisite u verziji koristeci apsolutnu putanju.


163. Zbog cega se koristi komanda ````cat > list1```` i koji ce biti rezultat?


164. Koja je razlika izmedju komande ````cat > list1```` i ````cat >> list1````


165. Koja je razlika izmedju `ls list*` i `ls *list`?


166. Koja je razlika izmedju `list?` i `?list` ?


167. Opisite komandu ````wc -l < dat > out````


168. Opisite komandu ````ls | head -1````


169. Opisite komandu ````ls | head -n 3 | tail -n 1````


170. Opisite komandu ````last reboot````


172. Kada koristimo komandu ````whoami````

173. Koja je razlike izmedju komandi ````lsof```` i ````lsof -u mysql````



175. Koje permisije postavlja komanda ````chmod 00000 test.sh````

176. Koje permisije posjeduje grupa na fajlu sa sljedecom reprezantacijom ````----------````?
