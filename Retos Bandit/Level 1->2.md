# Retos Bandit

# Level 1->2

## Objetivo
The password for the next level is stored in a file called **-** located in the home directory

## Datos de acceso al nivel
***Usuario:bandit1
Contraseña: NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

## Solucion
```bash

┌──(ulrich㉿DasMausoleum)-[~]
└─$ ssh bandit1@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _   
                        | |__   __ _ _ __   __| (_) |_ 
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_ 
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                                                       

                      This is an OverTheWire game server. 
            More information on http://www.overthewire.org/wargames

bandit1@bandit.labs.overthewire.orgs password:
  Enjoy your stay!

bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$ 

```


## Notas adicionales
Al iniciar una conexion nos manda a home/usuario. Ya no es necesario movernos.
## Referencias

