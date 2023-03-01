# Retos Bandit

## Objetivo
There are 2 files in the homedirectory: **passwords.old and passwords.new**. The password for the next level is in **passwords.new** and is the only line that has been changed between **passwords.old and passwords.new**

**NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19**

## Datos de acceso al nivel
***Usuario: bandit17
Contraseña:  ssh -i meinSchussel.txt bandit17@bandit.labs.overthewire.org -p 2220

![[meinSchussel.txt]]

## Solucion
```bash
┌──(ulrich㉿DasMausoleum)-[~]
└─$ nano  meinSchussel.txt                                          
                                                                                
┌──(ulrich㉿DasMausoleum)-[~]
└─$ ssh -i meinSchussel.txt bandit17@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _   
                        | |__   __ _ _ __   __| (_) |_ 
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_ 
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                                                       

                      This is an OverTheWire game server. 
            More information on http://www.overthewire.org/wargames

@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0644 for 'meinSchussel.txt' are too open.
It is required that your private key files are NOT accessible by others.
This private key will be ignored.
Load key "meinSchussel.txt": bad permissions
bandit17@bandit.labs.overthewire.org's password: 

zsh: suspended  ssh -i meinSchussel.txt bandit17@bandit.labs.overthewire.org -p 2220
                                                                                
┌──(ulrich㉿DasMausoleum)-[~]
└─$ sudo chmod 600 meinSchussel.txt 
[sudo] contraseña para ulrich: 
                                                                                
┌──(ulrich㉿DasMausoleum)-[~]
└─$ ssh -i meinSchussel.txt bandit17@bandit.labs.overthewire.org -p 2220

bandit17@bandit:~$ ls -la
total 36
drwxr-xr-x  3 root     root     4096 Feb 21 22:02 .
drwxr-xr-x 70 root     root     4096 Feb 21 22:04 ..
-rw-r-----  1 bandit17 bandit17   33 Feb 21 22:02 .bandit16.password
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit18 bandit17 3300 Feb 21 22:02 passwords.new
-rw-r-----  1 bandit18 bandit17 3300 Feb 21 22:02 passwords.old
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
drwxr-xr-x  2 root     root     4096 Feb 21 22:02 .ssh
bandit17@bandit:~$ cat /etc/bandit_pass/bandit17
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
bandit17@bandit:~$
---------------------------------------------------------------------------------
SEGUNDO PROCESO
---------------------------------------------------------------------------------
bandit17@bandit:~$ ls - la
ls: cannot access '-': No such file or directory
ls: cannot access 'la': No such file or directory
bandit17@bandit:~$ ls -la
total 36
drwxr-xr-x  3 root     root     4096 Feb 21 22:02 .
drwxr-xr-x 70 root     root     4096 Feb 21 22:04 ..
-rw-r-----  1 bandit17 bandit17   33 Feb 21 22:02 .bandit16.password
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit18 bandit17 3300 Feb 21 22:02 passwords.new
-rw-r-----  1 bandit18 bandit17 3300 Feb 21 22:02 passwords.old
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
drwxr-xr-x  2 root     root     4096 Feb 21 22:02 .ssh
bandit17@bandit:~$ diff password.old password.new
diff: password.old: No such file or directory
diff: password.new: No such file or directory
bandit17@bandit:~$ diff passwords.old passwords.new
42c42
< f9wS9ZUDvZoo3PooHgYuuWdawDFvGld2
---
> hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg

```

## Notas adicionales
## Referencias

