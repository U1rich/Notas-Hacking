# Retos Bandit

# Level 2->3

## Objetivo
The password for the next level is stored in a file called **spaces in this filename** located in the home directory.
## Datos de acceso al nivel
***Usuario: bandit2
Contraseña: rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
## Solucion
```bash
bandit2@bandit:~$ ls -la
total 24
drwxr-xr-x  2 root    root    4096 Feb 21 22:03 .
drwxr-xr-x 70 root    root    4096 Feb 21 22:04 ..
-rw-r--r--  1 root    root     220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root    root    3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root    root     807 Jan  6  2022 .profile
-rw-r-----  1 bandit3 bandit2   33 Feb 21 22:03 spaces in this filename
bandit2@bandit:~$ cd spaces_in_this_filename
-bash: cd: spaces_in_this_filename: No such file or directory
bandit2@bandit:~$ cat spaces_in_this_filename
cat: spaces_in_this_filename: No such file or directory
bandit2@bandit:~$ cat ./spaces_in_this_filename
cat: ./spaces_in_this_filename: No such file or directory
bandit2@bandit:~$ cat "spaces in this filename"
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$ 

```


## Notas adicionales
Para leer archivos con espacios se pueden usar:
archivo/ con/ espacio invertidos
"archivo con espacios"
'archivo con espacios'

## Referencias
https://linuxhandbook.com/filename-spaces-linux/
