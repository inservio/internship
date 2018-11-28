---
layout: default
title: Test1
parent: Tests
permalink: /docs/tests/test1/
---

{:toc}

# Pitanja



1. Opisati komandu ````which ls````



2. Opisati komandu `ls -a | grep '^.'`



3. Opisati komandu ````chmod -x cat.sh````



4. Opisati komandu ````ls -i /etc/passwd````



5. Opisati komandu ````ECHO $OLDPWD````


6. Opisati komandu ````find . -type f````


7. Sta predstavlja ````$OLDPWD```` u komadi ````ECHO $OLDPWD````?



8. Opisati komandu ````./cat.sh````




9. Koja je rezlika izmjedju komandi ````id -g root```` i ````id -G root````?



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



47. Sta je u primjeru ````ls -l /etc/passwd```` argument, sta je komanda, a sta je opcija?




53. Opisati komandu ````#!/usr/bin/env ruby````.


54. Opisati komandu ````grep root /etc/passwd | head -n 1````




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



152. Koja je razlika izmedju komande ````hostname```` i ````hostname -f````


156. Zbog cega izvrasavamo komandu ````echo $PATH````?


157. Zbog cega se koristi komanda ````find /tmp/ | wc -l````?

158. Sta znace skracenice ````STDIN````, ````STDOUT```` i ````STDERR````




161. Koja je razlika izmjedu ````head```` i ````tail```` komandi?




163. Zbog cega se koristi komanda ````cat > list1```` i koji ce biti rezultat?


164. Koja je razlika izmedju komande ````cat > list1```` i ````cat >> list1````





167. Opisite komandu ````wc -l < dat > out````


168. Opisite komandu ````ls | head -1````


169. Opisite komandu ````ls | head -n 3 | tail -n 1````


170. Opisite komandu ````last reboot````



173. Koja je razlike izmedju komandi ````lsof```` i ````lsof -u mysql````



175. Koje permisije postavlja komanda ````chmod 00000 test.sh````

176. Koje permisije posjeduje grupa na fajlu sa sljedecom reprezantacijom ````----------````?
