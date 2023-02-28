# Retos Bandit

## Objetivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

## Datos de acceso al nivel
***Usuario: bandit9
Contraseña: EN632PlfYiZbn3PhVK3XOGSlNInNE00t
## Solucion
```bash
bandit9@bandit:~$ ls -la
total 40
drwxr-xr-x  2 root     root     4096 Feb 21 22:02 .
drwxr-xr-x 70 root     root     4096 Feb 21 22:04 ..
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit10 bandit9 19379 Feb 21 22:02 data.txt
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
bandit9@bandit:~$ grep = data.txt 
grep: data.txt: binary file matches
bandit9@bandit:~$ grep "=" data.txt 
grep: data.txt: binary file matches
bandit9@bandit:~$ strings data.txt | grep -C 1  =
yjD<'`#
dS=5
fHK"
--
fs4l
f========== theM
s,<)
--
M-"c
=XeOh
/D8e
--
X1Q\
=vb`
|cW;ce
--
99lR
O=Nq
g-pT,
=I6a
r28w
--
A|9wE
========== password
)j;S2{
--
>0{MKqzdk
========== is
"6V-(
--
:cjJQ
2\:=
3LeJ
u=]T
caehl
--
%Af.Xr
%AM_9=
2[i|z
--
XY2Ck
1~=y
$OE~M
p>*!:
Q=9(
`&cl
--
V4<:
j=GD
;`ahG^$
--
d.TVk
b=fF
>8DUE
--
[K;+
0?F=(
?.Ws1op>
--
#e6I
.DX_/=
?+'g
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
8w51
bandit9@bandit:~$ 

```

## Notas adicionales
## Referencias

