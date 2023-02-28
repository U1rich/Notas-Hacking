# Retos Bandit

## Objetivo
The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.

## Datos de acceso al nivel
***Usuario: bandit4
Contraseña: 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe

## Solucion
```bash
bandit4@bandit:~$ ls -a
.  ..  .bash_logout  .bashrc  inhere  .profile
bandit4@bandit:~$ ls -la
total 24
drwxr-xr-x  3 root root 4096 Feb 21 22:03 .
drwxr-xr-x 70 root root 4096 Feb 21 22:04 ..
-rw-r--r--  1 root root  220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root root 3771 Jan  6  2022 .bashrc
drwxr-xr-x  2 root root 4096 Feb 21 22:03 inhere
-rw-r--r--  1 root root  807 Jan  6  2022 .profile
bandit4@bandit:~$ cd inhere/
bandit4@bandit:~/inhere$ ls -a
.   -file00  -file02  -file04  -file06  -file08
..  -file01  -file03  -file05  -file07  -file09
bandit4@bandit:~/inhere$ cat -file0
cat: invalid option -- 'f'
Try 'cat --help' for more information.
bandit4@bandit:~/inhere$ cat -/-file0
cat: invalid option -- '/'
Try 'cat --help' for more information.
bandit4@bandit:~/inhere$ cat ./-file0
cat: ./-file0: No such file or directory
bandit4@bandit:~/inhere$ cat ./-file00
=�M�Ð�EW�fbandit4@bandit:~/inhere$ cat ./-file01
��.Y>*���{K����H��G��[�o�Q�G�*�bandit4@bandit:~/inhere$ cat ./-file03
�Q]#�1���_�&5B���d�0^�]�D$�H�bandit4@bandit:~/inhere$ cat ./-file04
V���f���STA�܅�b�����U�kbandit4@bandit:~/inhere$ cat ./-file05
5�?:�o�ҫ\ԑ2s��=n̩-�`C9��`V�_�bandit4@bandit:~/inhere$ cat ./-file06
ЪF�`V��E+�sa��F�a\6n�0t��N+f
                            �bandit4@bandit:~/inhere$ cat ./-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: Non-ISO extended-ASCII text, with NEL line terminators
./-file06: Non-ISO extended-ASCII text, with no line terminators, with escape sequences
./-file07: ASCII text
./-file08: data
./-file09: data
bandit4@bandit:~/inhere$ 
```
## Notas adicionales
file tests each argument in an attempt to classify it.  There are three
     sets of tests, performed in this order: filesystem tests, magic tests,
     and language tests.  The first test that succeeds causes the file type to
     be printed.
## Referencias

