# Retos Bandit

## Objetivo
There is a git repository at `ssh://bandit28-git@localhost/home/bandit28-git/repo`. The password for the user `bandit28-git` is the same as for the user `bandit28`.

Clone the repository and find the password for the next level.

## Datos de acceso al nivel
***Usuario: bandit28
Contraseña: AVanL161y9rsbcJIsFHuw35rjaOM19nR

## Solucion
```bash
bandit28@bandit:/tmp/tmp.tb1oRWBrBE$ cd ..
bandit28@bandit:/tmp$ cd ..
bandit28@bandit:/$ ls
bin   drifter     home     lib32   lost+found  opt   run   srv  usr
boot  etc         krypton  lib64   media       proc  sbin  sys  var
dev   formulaone  lib      libx32  mnt         root  snap  tmp
bandit28@bandit:/$ cd ~
bandit28@bandit:~$ ls
bandit28@bandit:~$ ls -la
total 20
drwxr-xr-x  2 root root 4096 Feb 21 22:02 .
drwxr-xr-x 70 root root 4096 Feb 21 22:04 ..
-rw-r--r--  1 root root  220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root root 3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root root  807 Jan  6  2022 .profile
bandit28@bandit:~$ cd /tmp/tmp.tb1oRWBrBE
bandit28@bandit:/tmp/tmp.tb1oRWBrBE$ git clone ssh://bandit28-git@localhost:2220/home/bandit28-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit28/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit28/.ssh/known_hosts).
                         _                     _ _ _   
                        | |__   __ _ _ __   __| (_) |_ 
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_ 
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                                                       

                      This is an OverTheWire game server. 
            More information on http://www.overthewire.org/wargames

bandit28-git@localhost's password: 
remote: Enumerating objects: 9, done.
remote: Counting objects: 100% (9/9), done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 9 (delta 2), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (9/9), done.
Resolving deltas: 100% (2/2), done.
bandit28@bandit:/tmp/tmp.tb1oRWBrBE$ ls
repo
bandit28@bandit:/tmp/tmp.tb1oRWBrBE$ cd repo
bandit28@bandit:/tmp/tmp.tb1oRWBrBE/repo$ ls -la
total 16
drwxrwxr-x 3 bandit28 bandit28 4096 Mar  7 18:56 .
drwx------ 3 bandit28 bandit28 4096 Mar  7 18:56 ..
drwxrwxr-x 8 bandit28 bandit28 4096 Mar  7 18:56 .git
-rw-rw-r-- 1 bandit28 bandit28  111 Mar  7 18:56 README.md
bandit28@bandit:/tmp/tmp.tb1oRWBrBE/repo$ cat README.md 
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: xxxxxxxxxx

bandit28@bandit:/tmp/tmp.tb1oRWBrBE/repo$ cd git
-bash: cd: git: No such file or directory
bandit28@bandit:/tmp/tmp.tb1oRWBrBE/repo$ cd .git
bandit28@bandit:/tmp/tmp.tb1oRWBrBE/repo/.git$ ls -la
total 52
drwxrwxr-x 8 bandit28 bandit28 4096 Mar  7 18:56 .
drwxrwxr-x 3 bandit28 bandit28 4096 Mar  7 18:56 ..
drwxrwxr-x 2 bandit28 bandit28 4096 Mar  7 18:56 branches
-rw-rw-r-- 1 bandit28 bandit28  281 Mar  7 18:56 config
-rw-rw-r-- 1 bandit28 bandit28   73 Mar  7 18:56 description
-rw-rw-r-- 1 bandit28 bandit28   23 Mar  7 18:56 HEAD
drwxrwxr-x 2 bandit28 bandit28 4096 Mar  7 18:56 hooks
-rw-rw-r-- 1 bandit28 bandit28  137 Mar  7 18:56 index
drwxrwxr-x 2 bandit28 bandit28 4096 Mar  7 18:56 info
drwxrwxr-x 3 bandit28 bandit28 4096 Mar  7 18:56 logs
drwxrwxr-x 4 bandit28 bandit28 4096 Mar  7 18:56 objects
-rw-rw-r-- 1 bandit28 bandit28  114 Mar  7 18:56 packed-refs
drwxrwxr-x 5 bandit28 bandit28 4096 Mar  7 18:56 refs
bandit28@bandit:/tmp/tmp.tb1oRWBrBE/repo/.git$ git log
commit 104db85a904e9691ff22aafe1a96124c88f75afa (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    fix info leak

commit 6c3c5e485cc531e5d52c321587ce1103833ab7c3
Author: Morla Porla <morla@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    add missing data

commit cd3b97ef95879ec34df0d6c82f2a96d552f0e56c
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    initial commit of README.md
bandit28@bandit:/tmp/tmp.tb1oRWBrBE/repo/.git$ git checkout 6c3c5e485cc531e5d52c321587ce1103833ab7c3
fatal: this operation must be run in a work tree
bandit28@bandit:/tmp/tmp.tb1oRWBrBE/repo/.git$ cd ..
bandit28@bandit:/tmp/tmp.tb1oRWBrBE/repo$ git checkout 6c3c5e485cc531e5d52c321587ce1103833ab7c3
Note: switching to '6c3c5e485cc531e5d52c321587ce1103833ab7c3'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 6c3c5e4 add missing data
bandit28@bandit:/tmp/tmp.tb1oRWBrBE/repo$ cat README.md 
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S

bandit28@bandit:/tmp/tmp.tb1oRWBrBE/repo$ 
```

## Notas adicionales


## Referencias


