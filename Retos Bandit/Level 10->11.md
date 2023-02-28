# Retos Bandit

## Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data.

## Datos de acceso al nivel
***Usuario: bandit10
Contraseña: G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

## Solucion
```bash
bandit10@bandit:~$ ls -la
total 24
drwxr-xr-x  2 root     root     4096 Feb 21 22:02 .
drwxr-xr-x 70 root     root     4096 Feb 21 22:04 ..
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit11 bandit10   69 Feb 21 22:02 data.txt
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ base64 --help
Usage: base64 [OPTION]... [FILE]
Base64 encode or decode FILE, or standard input, to standard output.

With no FILE, or when FILE is -, read standard input.

Mandatory arguments to long options are mandatory for short options too.
  -d, --decode          decode data
  -i, --ignore-garbage  when decoding, ignore non-alphabet characters
  -w, --wrap=COLS       wrap encoded lines after COLS character (default 76).
                          Use 0 to disable line wrapping

bandit10@bandit:~$ base64 -d data.txt 
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$ 

```

## Notas adicionales
**Base 64 es un sistema de numeración posicional que usa 64 como base**. Es la mayor potencia que puede ser representada usando únicamente los caracteres imprimibles de ASCII. Esto ha propiciado su uso para codificación de correos electrónicos, PGP y otras aplicaciones. Todas las variantes famosas que se conocen con el nombre de Base64 usan el rango de caracteres _A-Z, a-z y 0-9_ en este orden para los primeros 62 dígitos, pero los símbolos escogidos para los últimos dos dígitos varían considerablemente de unas a otras. Algunos de los usos de la codificación son; _la compresión de datos, la ocultación de datos o la transmisión de datos en otro formato_.
## Referencias
https://ubunlog.com/base64-codificacion-decodificacion-terminal/