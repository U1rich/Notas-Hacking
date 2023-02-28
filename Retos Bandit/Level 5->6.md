# Retos Bandit

## Objetivo
The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:



## Datos de acceso al nivel
***Usuario: bandit5
Contraseña: lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

## Solucion
```bash
bandit5@bandit:~$ ls -la
total 24
drwxr-xr-x  3 root root    4096 Feb 21 22:03 .
drwxr-xr-x 70 root root    4096 Feb 21 22:04 ..
-rw-r--r--  1 root root     220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root root    3771 Jan  6  2022 .bashrc
drwxr-x--- 22 root bandit5 4096 Feb 21 22:03 inhere
-rw-r--r--  1 root root     807 Jan  6  2022 .profile
bandit5@bandit:~$ cd inhere
bandit5@bandit:~/inhere$ ls
maybehere00  maybehere04  maybehere08  maybehere12  maybehere16
maybehere01  maybehere05  maybehere09  maybehere13  maybehere17
maybehere02  maybehere06  maybehere10  maybehere14  maybehere18
maybehere03  maybehere07  maybehere11  maybehere15  maybehere19
bandit5@bandit:~/inhere$ find . -readable -type f -size 1033c
./maybehere07/.file2
bandit5@bandit:~/inhere$ cd maybehere
-bash: cd: maybehere: No such file or directory
bandit5@bandit:~/inhere$ cd maybehere07
bandit5@bandit:~/inhere/maybehere07$ ls
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3
bandit5@bandit:~/inhere/maybehere07$ ls -la
total 56
drwxr-x---  2 root bandit5 4096 Feb 21 22:03 .
drwxr-x--- 22 root bandit5 4096 Feb 21 22:03 ..
-rwxr-x---  1 root bandit5 3663 Feb 21 22:03 -file1
-rwxr-x---  1 root bandit5 3065 Feb 21 22:03 .file1
-rw-r-----  1 root bandit5 2488 Feb 21 22:03 -file2
-rw-r-----  1 root bandit5 1033 Feb 21 22:03 .file2
-rwxr-x---  1 root bandit5 3362 Feb 21 22:03 -file3
-rwxr-x---  1 root bandit5 1997 Feb 21 22:03 .file3
-rwxr-x---  1 root bandit5 4130 Feb 21 22:03 spaces file1
-rw-r-----  1 root bandit5 9064 Feb 21 22:03 spaces file2
-rwxr-x---  1 root bandit5 1022 Feb 21 22:03 spaces file3
bandit5@bandit:~/inhere/maybehere07$ cat .file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

```
## Notas adicionales
## Referencias

