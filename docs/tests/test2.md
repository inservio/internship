---
layout: default
title: Test2    
parent: Tests
permalink: /docs/tests/test2/
---



1. Ako uzmemo u obzir da je username trenutno logovanog korisnika tux, koja je apsulutna putanja sljedece relativne putanje ~/.ssh/. ?

2. Sadrzaj kojeg direktorija ce biti prikazan nakon izvrsenja komande?

````
ls /../../../../..
````

3. Sta je cilj sljedece komande?

````
PATH=$PATH:/var/www
````

4. Sadrzaj kojeg direktorija ce biti prikazan nakon izvrsenja sljedece komande?

````
ls /./././
````

5. Koja je razlika izmedju komande ````ls $HOME/.ssh/````  i  ````ls ~/.ssh/```` ?


6. Sta ce vratiti sljedeca komanda ls . | grep '^\.'

7. Koji ce korisnik biti prikazan na ispisu komande cat /etc/passwd | grep ':0:' ?

8. Opisati komandu ls ~/. | sort -R

9. Napisati apsolutnu putanju direktorija koji ce postati current directory nakon izvrsenja komande u nastavku.

web7@server:~$ cd /home/$USER

10. Koji je razultat komande ls /. >> ./ls ?

11. Zasto se portovi dijele u privilegovane i u neprivilegovane?

12. Koji je rezultat sljedece komande tail -n 100 /dev/null

13. Koji je rezultat sljedece komande head -n 100 /dev/null

14. Sta predstavlja znak | u komandi grep 'MemFree\|MemTotal'

15. Sta predstavlja direktorij /proc ?

16. Koji numericki ID ce biti rezultat sljedece komande cat /proc/1/status | grep -w 'Pid' ?

17. Koje informacije nam daje komanda uname -a ?

18. Sta oznacuje /dev/sda a sta /dev/sda1 te koja je njihova povezanost ?

19. Sta je postize komanda touch /.test ?

20. Napisati apsolutnu putanju fajla kojeg ce napraviti komanda touch /.test

21. Da li ce nekoliko puta ponovljena komanda curl 'http://google.com:80/fajl.pdf' >> fajl.pdf rezultirati validnim fajlom? Objasniti.

22. U kojem konfiguracijskom fajlu je podesen hostname?

23. U kojem konfiguracijskom fajlu je podesena IP adresa za hostname?

24. Koje su prednosti i mane RAID0?

25. Komandu ls ~/../. napisite u verziji koristeci apsolutnu putanju, trenutno logovani korisnik je neprivilegovani korisnik.

26. U slucaju da je trenutno prijavljeni korinik root, koja je apsulutna putanja u slucaju ls ~/../ komande


27. Sta se desava sa fajlom imena source nakon ispod izvrsenih komandi?

touch source
ln -s source destination
rm destination

28. Koji ce rezultat biti zadnje izvrsene komande?

su root
su root
exit
whoami

29. Koji je rezultat komande ls . | tail -n 0 | wc -l > ls ?

30. Objasniti sljedecu komandu cat /proc/cpuinfo | grep -w 'processor' | wc -l

31. Koja je razlika izmedju simbolickih i hard linkova?

32. Koja je svrha komande mount -l ?

33. Koji ce biti sadrzaj i velicina u Bajtima datoteke dat.out nakon sto je izvrsena komanda cat /dev/null > dat.out ?

34. Sta znaci skracenica PID ?

35. Koja je razlika izmedju koandi free -m i free -g ?

36. Objasniti komandu `ls -l *.txt` ukljucujuci i njene opcije.

37. Koja je prva linija perl skripte?

38. Koja je prva linija bash skripte?

39. Koja je prva linija ruby skripte?

40. Komanda cat /proc/meminfo | grep MemTotal prikazuje 5 GB RAM memorije, dok komanda free -t prikazuje 11 GB RAM memorije. Zasto?


41. Opisati fajl /etc/services

42. Koja je svrha fajla /etc/aliases

43. Da li ce nekoliko puta ponovljena komanda curl 'http://google.com:80/fajl.pdf' > fajl.pdf rezultirati validnim fajlom? Objasniti.
