---
layout: default
title: Test1
parent: Tests
permalink: /docs/tests/test1/
---



# Pitanja

1. Sta je znaci akronim odnosno komanda

````
cd?
````



2. Sta je znaci akronim odnosno komanda ````ls````?




3. Sta je znaci akronim odnosno komanda ````pwd````?




4. Opsati komandu ````cd .````




5. Opisati komandu ````cd ..````




6. Opisati komandu ````cd ../..````




7. Opisati komandu ````cd /````



8. Koji je ovo tip datoteke ````-rw-r--r--```` ?




9. Opisati komandu ````cd ~````




10. Opisati komandu ````cd -````




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



22. Navesti tri razlicita nacina ulaska u home direktorij korisnika?



23. Opisati komandu ````./cat.sh````




24. Naposljetku u kojem direktoriju ce rezultirati sljedeci niz komandi? ````cd ~ ; cd /tmp; cd $OLDPWD````



25. Koja je rezlika izmjedju komandi ````id -g root```` i ````id -G root````?





26. Gdje se nalazi sljedeca fatoteka ````~/.bashrc```` ?




27. Koji je ovo tip datoteke ````dr-xr-xr-x````?




28. Navesti primjer ````apsolutne```` i ````relativne```` putanje.




29. Kojom komandom proveravamo koji je ````SHELL```` podesen za trenutnog korisnika?





30. Opisati komandu ````find . -type d````





31. Opisati komandu ````man find````




32. Opisati komandu ````whereis -b bash````




33. Opisati komandu ````whereis -m bash````




34. Cime se rezultirati sljedeca komanda ````mkdir /tmp/sta/ima/danas/kod/tebe/druze/moj```` ? Zasto?




35. Sta ce biti rezultat komande ````id -g root````?




36. Opisati komandu ````su korisnik -l````




37. Opisati komandu ````cp -p kakoje.rb kakoje2.rb````




38. Sta predstavlja ````#!/bin/bash````




39. Na kojoj liniji unutar fajla se nalazi ````#!/bin/bash````?




40. Kako se popularno nazivaju znakovi ````#!```` u sljedecem primjeru ````#!/bin/bash```` ?




41. Opisati komandu ````chmod +x cat.sh````.




42. Sta predstavlja direktorij ````/root````?



43. Sta predstavlja direktorij ````/etc````?



44. Sta predstavlja direktorij ````/opt````?



45. Sta predstavlja direktorij ````/mnt````?



46. Sta predstavlja direktorij ````/tmp````?



47. Sta je u primjeru ````ls -l /etc/passwd```` argument, sta je komanda, a sta je opcija?



48. Za sta sluzi komnda ````type````?



49. Sta postize komanda ````touch 'kakoje'````?



50. Zasto koristimo jednostruke navodnike u komandu ````touch 'kako je'````




51. Koji je ovo tip datoteke ````lrwxr-xr-x@````




52. Zasto dobijamo sljedecu gresku?
```
$ ./cat.sh
-bash: ./cat.sh: Permission denied
```  





53. Opisati komandu ````#!/usr/bin/env ruby````.




54. Opisati komandu ````grep root /etc/passwd | head -n 1````




55. Sta ce biti rezultat komande ````id -u root```` ?




56. Opisati ````-p```` u komandi ````mkdir -p /tmp/dobar/dan/je/danas````




57. Sta se desi sa sadrzajem direktorija ````/tmp```` nakon reboota?




58. Opisati komandu ````who````



59. Kako se zove specijalni znak ````\```` u komandi ````ls /tmp/Dimu\ Borgir/````?




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





66. Koje podatke dobijamo kao rezultat komande ````ping google.com````?




67. Koji protokol koristi komanda ````ping````?




68. Objasniti opciju ````-c 4```` u komandi ````ping -c 4 google.com````?




69. Objasniti opciju ````-4 ```` u komandu ````ping -4 google.com````.




70. Navesti primjer privatne IP adrese.




71. Sta predstavlja ````NAT````




72. Na koji IP resolva hostname ````localhost````?




73. Opisati komandu ````nslookup google.com````




74. Na kojem portu sluza ````DNS````?




75. Kako se zove specijalni znak ````|```` u komandi ````ls | sort````




76. Opisati komandu ````ls | sort -n````




77. Koji je razultat komande ````ls . > ls````?




78. Navesti dva protokola ````Transport layera````




79. Navesti nekoliko protokola ````Application layera````



80. Koju IP adresu ce prikazati komanda ````ifconfig lo````?



81. Kako se naziva ````lo```` device u komandi ````ifconfig lo````



82. Koju IP adresu ce rezolvati komanda ````ping -4 localhost````?



83. Sta predstavlja ````/24```` u izrazu ````192.0.2.0/24````?



84. Koji je raspon privilegovanih portova?



85. Koji je raspon neprivilegovanih portova?



86. Na kojem portu slusa ````HTTP```` protokol?



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



103. Koja je glavna prednost ````SSH```` protokola u odnosu na ````TELNET````?



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



110. Da li svi korisnici imaju dozvolje da pisu u ````*/tmp````* direktorij? Zaokruziti.  
   A. DA  
   B. NE  

111. Da li svi korisnici imaju permisije da brisu sve fajlove u ````/tmp```` direktoriju? Zaokruziti.



112. IP adresa korisnikovog racunara je ````192.168.0.55````. Koja je po konvenciji IP adresa routera?



113. Na koja dva ````transport layera```` operira DNS protokol?



114. Koja je svrha ````DHCP```` protokola?



115. Na kojem mreznom uredjaju je podesen ````DHCP```` servis?



116. Navesti minimalno jedan port na kojem slusa ````SMTP```` protokol.



117. Virtuelna masini je dodijelna javna IP adresa ````128.53.99.170````. Kojom komandom saznati na kojem serveru se nalazi ta virtuelna masina?


118. Sta predstavlja ````300```` HTTP status code?


119. Sta predstavlja ````400```` HTTP status code?


120. Sta predstavlja ````500```` HTTP status code?

121. Sta predstavlja ````200```` HTTP status code?

122. Opisati komandu ````lsblk````

123. Opisati komandu ````fdisk -l````

124. Koja ja namjena komande ````mkfs.ext4````

125. Opisati komandu ````mount /dev/sdc /mnt/sdc/````

126. Za sta sluzi fajl ````/etc/fstab````?

127. Opisati komandu ````blkid````

128. Razlika izmedju komande ````apt-get update```` i ````apt-get upgrade````

129. Cemu sluzi komanda ````dpkg-reconfigure tzdata````

130. Sta ispisuje komanda ````date````?

131. Za sta sluzi komanda ````git clone```` ?

132. Opisati komandu ````mkdir .chef````

133. Opisati komandu ````cat /home/rails/.ssh/id_rsa.pub````

134. Sta radi komanda ````curl 'http://google.com:80/fajl.pdf' > fajl.pdf```` te preko kojeg protokola i porta?

135. Zbog cega koristimo ````sudo```` komandu?

136. Sta radi komanda ````Location="westeurope"```` u bash shellu?


137. Sta znaci skracenica ````FQDN````

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

151. Objasniti gresku u sljedecem primjeru.
````touch /tmp/CAO````
````rm /tmp/cao````
````rm: /tmp/cao: No such file or directory````

152. Koja je razlika izmedju komande ````hostname```` i ````hostname -f````

153. Koji ````SHELL```` koristi korisnik u sljedecem primjeru?
````nobody:*:-2:-2:Unprivileged User:/var/empty:/usr/bin/false````


154. Koji direktorij je postavljen za home u sljedecem primjeru te za kojeg korisnika?
````mail:x:8:8:mail:/var/mail:/usr/sbin/nologin````

155. Na kojem mjestu u sljedecem primjeru bi se trebao nalaziti password?  
````web138:x:5006:5007::/var/www/clients/client110/web138:/bin/false````

156. Zbog cega izvrasavamo komandu ````echo $PATH````?


157. Zbog cega se koristi komanda ````find /tmp/ | wc -l````?

158. Sta znace skracenice ````STDIN````, ````STDOUT```` i ````STDERR````

159. Sta se nalazi u direktorijumu ````/dev````?

160. Koji je rezultat sljedece skripte?  
````
if [ 1 -gt 100 ]  
then  
echo 'TRUE'  
else  
echo 'FALSE'  
fi  
````

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

171. Opisite komandu ````hostname -I````

172. Kada koristimo komandu ````whoami````

173. Koja je razlike izmedju komandi ````lsof```` i ````lsof -u mysql````

174. Sta predstavljaju skracenice ````eth0```` i ````eth1````

175. Kada koristimo komandu ````host 173.194.76.27```` tj ````host IP_ADRESA````

175. Koje permisije postavlja komanda ````chmod 00000 test.sh````

176. Koje permisije posjeduje grupa na fajlu sa sljedecom reprezantacijom ````----------````?

177. Koji je rezultat sljedece skripte?  
````
if [ 1 -lt 100 ]  
then  
echo 'TRUE'  
else  
echo 'FALSE'  
fi  
````

178. Koji je rezultat sljedece skripte?
````
if [ 100 -eq 100 ]  
then  
echo 'TRUE'  
else  
echo 'FALSE'  
fi
````

179. Koji je rezultat sljedece skripte?
````
if [ 100 -ne 100 ]  
then  
echo 'TRUE'  
else  
echo 'FALSE'  
fi
````

180. Koji je rezultat sljedece skripte?
````
if [ 100 -ge 100 ]  
then  
echo 'TRUE'  
else  
echo 'FALSE'  
fi
````



181. Koji je rezultat sljedece skripte?
````
if [ 100 -le 100 ]  
then  
echo 'TRUE'  
else  
echo 'FALSE'  
fi
````



182. Koji je rezultat sljedece skripte?
````
if [ 1 -ge 100 ] || [ 100 -eq 100 ]
then  
echo 'TRUE'  
else  
echo 'FALSE'  
fi
````


183. Koji je rezultat sljedece skripte?
````
if [ 1 -ge 100 ] && [ 100 -eq 100 ]
then  
echo 'TRUE'  
else  
echo 'FALSE'  
fi
````
