# Retos Bandit

## Objetivo

## Datos de acceso al nivel
***Usuario: bandit10
Contraseña: G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
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

```

## Notas adicionales
## Referencias

