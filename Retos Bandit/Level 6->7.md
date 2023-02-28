# Retos Bandit

## Objetivo
The password for the next level is stored **somewhere on the server** and has all of the following properties:

-   owned by user bandit7
-   owned by group bandit6
-   33 bytes in size

## Datos de acceso al nivel
***Usuario: bandit6
Contraseña: P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

## Solucion
```bash
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat }
cat: '}': No such file or directory
bandit6@bandit:~$ cat /var/l
lib/   local/ lock/  log/   
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password 
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
bandit6@bandit:~$ 
```

## Notas adicionales
Tuve que usar su ayuda hehe

## Referencias
https://ingsoftware.reduaz.mx/moodle/pluginfile.php/68106/mod_resource/content/2/05-retos-bandit-p2.pdf

