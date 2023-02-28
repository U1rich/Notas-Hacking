# Retos Bandit

## Objetivo

## Datos de acceso al nivel
***Usuario: bandit8
Contraseña: TESKZC0XvTetK0S9xNwm25STk5iWrBvP
## Solucion
```bash
bandit8@bandit:~$ ls -la
total 56
drwxr-xr-x  2 root    root     4096 Feb 21 22:03 .
drwxr-xr-x 70 root    root     4096 Feb 21 22:04 ..
-rw-r--r--  1 root    root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root    root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit9 bandit8 33033 Feb 21 22:03 data.txt
-rw-r--r--  1 root    root      807 Jan  6  2022 .profile
bandit8@bandit:~$ cat data.txt 
.
.
.
TNivxqvFn7mIfQh3cTALiTwEBgIDmArp
8cxHNGSfzmAu3VgEYDqhvT5uK41lmKzx
bandit8@bandit:~$ wc data.txt 
 1001  1001 33033 data.txt
bandit8@bandit:~$ cat data.txt | uniq -u
2QIjuO3vCFLMh13odiJQrsCNZGEABZXw
vFGqJHMFuFOE70HhGPn2SPdMFwUO8mlw
.
.
.
bandit8@bandit:~$ cat data.txt | sort  uniq -u
.bash_logout  .bashrc       data.txt      .profile      
bandit8@bandit:~$ cat data.txt | sort | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
bandit8@bandit:~$ 

```

## Notas adicionales
## Referencias

