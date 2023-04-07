## Descripción

There's an interesting script in the user's home directory The work computer is running SSH. We've been given a script which performs some basic calculations, explore the script and find a flag.

```
Hostname: saturn.picoctf.net
Port:     58184
Username: picoplayer
Password: password
```

## Hints

## Solución

Conectarse mediante ssh: `ssh picoplayer@saturn.picoctf.net -p 58184`

```
picoplayer@challenge:~$ ls -la
total 16
drwxr-xr-x 1 picoplayer picoplayer   20 Mar 20 05:40 .
drwxr-xr-x 1 root       root         24 Mar 16 02:30 ..
-rw-r--r-- 1 picoplayer picoplayer  220 Feb 25  2020 .bash_logout
-rw-r--r-- 1 picoplayer picoplayer 3771 Feb 25  2020 .bashrc
drwx------ 2 picoplayer picoplayer   34 Mar 20 05:40 .cache
-rw-r--r-- 1 picoplayer picoplayer  807 Feb 25  2020 .profile
-rwxr-xr-x 1 root       root        517 Mar 16 01:30 useless
picoplayer@challenge:~$ file useless 
useless: Bourne-Again shell script, ASCII text executable
picoplayer@challenge:~$ cat useless 
#!/bin/bash
# Basic mathematical operations via command-line arguments
...
```

Al analizar el script nos damos cuenta que solamente se ejecuta si le enviamos 3 argumentos y ejecuta operaciones matemáticas simples, pero no hace nada especial. Hacia el final del archivo nos dice que leamos el manual, por lo que ejecutamos el comando `man useless` y obtenemos la bandera

```
picoplayer@challenge:~$ man useless 

useless
     useless, -- This is a simple calculator script

SYNOPSIS
     useless, [add sub mul div] number1 number2

DESCRIPTION
     Use the useless, macro to make simple calulations like addition,subtraction, multiplication and division.

Examples
     ./useless add 1 2
       This will add 1 and 2 and return 3

     ./useless mul 2 3
       This will return 6 as a product of 2 and 3

     ./useless div 6 3
       This will return 2 as a quotient of 6 and 3

     ./useless sub 6 5
       This will return 1 as a remainder of substraction of 5 from 6

Authors
     This script was designed and developed by Cylab Africa

     picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_5562}
```

## Bandera

```
picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_5562}
```

## Notas adicionales

## Referencias
