# Retos Bandit

## Objetivo
There is a git repository at `ssh://bandit30-git@localhost/home/bandit30-git/repo`. The password for the user `bandit30-git` is the same as for the user `bandit30`.

Clone the repository and find the password for the next level.

## Datos de acceso al nivel
***Usuario: bandit30
Contraseña: xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS

## Solucion
```bash
bandit30@bandit:~$ mktemp -d
/tmp/tmp.fPClj2pDJV
bandit30@bandit:~$ cd /tmp/tmp.fPClj2pDJV

bandit30@bandit:/tmp/tmp.fPClj2pDJV$ git clone ssh://bandit30-git@localhost:2220/home/bandit30-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit30/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit30/.ssh/known_hosts).
                         _                     _ _ _   
                        | |__   __ _ _ __   __| (_) |_ 
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_ 
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                                                       

                      This is an OverTheWire game server. 
            More information on http://www.overthewire.org/wargames

bandit30-git@localhost's password: 
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
Receiving objects: 100% (4/4), 298 bytes | 298.00 KiB/s, done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
bandit30@bandit:/tmp/tmp.fPClj2pDJV$ repo
Command 'repo' not found, but can be installed with:
snap install git-repo  # version 1.12.37-3, or
apt  install repo      # version 2.17.3-3
See 'snap info git-repo' for additional versions.
bandit30@bandit:/tmp/tmp.fPClj2pDJV$ cd repo
bandit30@bandit:/tmp/tmp.fPClj2pDJV/repo$ ls
README.md
bandit30@bandit:/tmp/tmp.fPClj2pDJV/repo$ car README.md 
Command 'car' not found, but can be installed with:
apt install ucommon-utils
Please ask your administrator.
bandit30@bandit:/tmp/tmp.fPClj2pDJV/repo$ cat README.md 
just an epmty file... muahaha
bandit30@bandit:/tmp/tmp.fPClj2pDJV/repo$ git log
commit cf552c166d78421e64ddf52f850e680075d216e1 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:13 2023 +0000

    initial commit of README.md
bandit30@bandit:/tmp/tmp.fPClj2pDJV/repo$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
bandit30@bandit:/tmp/tmp.fPClj2pDJV/repo$ git log
commit cf552c166d78421e64ddf52f850e680075d216e1 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:13 2023 +0000

    initial commit of README.md
bandit30@bandit:/tmp/tmp.fPClj2pDJV/repo$ git checkout remotes/origin/master
Note: switching to 'remotes/origin/master'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at cf552c1 initial commit of README.md
bandit30@bandit:/tmp/tmp.fPClj2pDJV/repo$ cat README.md 
just an epmty file... muahaha
bandit30@bandit:/tmp/tmp.fPClj2pDJV/repo$ git tag
secret
bandit30@bandit:/tmp/tmp.fPClj2pDJV/repo$ git show secret 
OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
bandit30@bandit:/tmp/tmp.fPClj2pDJV/repo$ 

```

## Notas adicionales


## Referencias

