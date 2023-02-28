# Retos Bandit

## Objetivo
The password for the next level is stored in the file **data.txt** next to the word **millionth**

## Datos de acceso al nivel
***Usuario: bandit7
Contraseña: z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

## Solucion
```bash
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ cat data.txt | find "millionth"
find: ‘millionth’: No such file or directory
bandit7@bandit:~$ cat data.txt
godless	pnXYVum26z4FI2NGF4OTheIeiEs9zUN8
sclerosis's	gmFYBgwwk7ML0MExzml95jwxoh2a76Af
nurturing	OMN5jKbXJqlJZkuyPhGyDt7gvZ0GBdvk
associates	8zDpfUQpqc2uTzC0PonPuwkt5miSPMhh
spiritualistic	KlhvAfX8oPz96nnQx5iKOsHadebKcz1t
reload	Lhpafa9xDrXDg4LhE5ta7RlWPBq8o6A5
Pennsylvanians	xPjtq5JXaM4I37lUUziLiS92UuwR9TAT
Arno's	yTanS438cGlD254MhoS6gO8D1MR5J3EA
forewarning	ikxZCvPdGs1gGKyhZ3icuR0yUGcQPGcx
trader	qOO6OQNIH4aPesdcS7SfUZV4cuqwQ7zX
fizz	NTCKTry02qTzzD0B9kpfLgv72reCKv2Q
grosbeak	XlZ4xdTAxKaaXNEcSzUVNKvqZWocg8Ob
rivaling	ed25fsTNwvmqu5P0yE0ODfdBrfJe48Su
Marlon's	Ey3K4febMqvQgsLImm18HqrkmK1aWkaE
Tweed's	V5td37AgOmpsgmF1T3HC4JwrEzhZsiey
bandit7@bandit:~$ cat data.txt | grep millionth
millionth	TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$ 

```

## Notas adicionales

## Referencias
https://geekland.eu/uso-del-comando-grep-en-linux-y-unix-con-ejemplos/

