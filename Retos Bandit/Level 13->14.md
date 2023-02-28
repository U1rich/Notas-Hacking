# Retos Bandit

## Objetivo
The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. **Note:** **localhost** is a hostname that refers to the machine you are working on

## Datos de acceso al nivel
***Usuario: bandit13
Contraseña: wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
## Solucion
```bash
bandit13@bandit:~$ ls -la
total 24
drwxr-xr-x  2 root     root     4096 Feb 21 22:02 .
drwxr-xr-x 70 root     root     4096 Feb 21 22:04 ..
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
-rw-r-----  1 bandit14 bandit13 1679 Feb 21 22:02 sshkey.private
bandit13@bandit:~$ ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
The authenticity of host '[bandit.labs.overthewire.org]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes

...
bandit14@bandit:~$ ls
bandit14@bandit:~$ ls -la
total 24
drwxr-xr-x  3 root root 4096 Feb 21 22:02 .
drwxr-xr-x 70 root root 4096 Feb 21 22:04 ..
-rw-r--r--  1 root root  220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root root 3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root root  807 Jan  6  2022 .profile
drwxr-xr-x  2 root root 4096 Feb 21 22:02 .ssh
bandit14@bandit:~$ /
-bash: /: Is a directory
bandit14@bandit:~$ cd /
bandit14@bandit:/$ ls
bin  boot  dev  drifter  etc  formulaone  home  krypton  lib  lib32  lib64  libx32  lost+found  media  mnt  opt  proc  root  run  sbin  snap  srv  sys  tmp  usr  var
bandit14@bandit:/$ cd etc
bandit14@bandit:/etc$ ls

...
dbus-1                         hostname            ld.so.conf                  nanorc          rc0.d                   sudoers
debconf.conf                   hosts               ld.so.conf.d                needrestart     rc1.d                   sudoers.d
bandit14@bandit:/etc$ find pass
find: ‘pass’: No such file or directory
bandit14@bandit:/etc$ find bandit
find: ‘bandit’: No such file or directory
bandit14@bandit:/etc$ ls -la
total 1052
drwxr-xr-x 108 root     root      12288 Feb 21 22:04 .
drwxr-xr-x  22 root     root       4096 Feb 24 22:58 ..

...
-rw-r--r--   1 root     root        460 Dec  8  2021 zsh_command_not_found
bandit14@bandit:/etc$ cd bandit_pass/
bandit14@bandit:/etc/bandit_pass$ ls -la
total 152

...
-r--------   1 bandit8  bandit8     33 Feb 21 22:02 bandit8
-r--------   1 bandit9  bandit9     33 Feb 21 22:02 bandit9
bandit14@bandit:/etc/bandit_pass$ cat bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
bandit14@bandit:/etc/bandit_pass$ 


```

## Notas adicionales
## Referencias

