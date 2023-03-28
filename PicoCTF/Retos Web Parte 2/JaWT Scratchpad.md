## Objetivo
Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/63090/` or http://jupiter.challenges.picoctf.org:63090

## Hints

## Solución
Para solucionar este reto fue necesario logearse con cualquier nombre para generar el json de la cookie y poder modificarla mediante la pagina JWT.io.
Al momento de modificar da error si lo unico que hacemos es enviar el nombre de admin pero sin la contraseña asi que procedemos a crackearla de esta manera:

```bash
Primero creamon un archivo con la clave y le pegamos la cookie:
└─$ nano encriptado

Finalmene usamos john y rockyou.txt para buscar la clave:

┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/HackNotes]
└─$ john encriptado -w=/usr/share/wordlists/rockyou.txt
Using default input encoding: UTF-8
Loaded 1 password hash (HMAC-SHA256 [password is key, SHA256 128/128 AVX 4x])
Will run 4 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
ilovepico        (?)     
1g 0:00:00:05 DONE (2023-03-28 00:30) 0.1968g/s 1456Kp/s 1456Kc/s 1456KC/s iloverob4live345..ilovemymother@
Use the "--show" option to display all of the cracked passwords reliably
Session completed. 

```
al final solo guardamos esa cookie y refrescamos la pagina.

### picoCTF{jawt_was_just_what_you_thought_f859ab2f}
## Notas adicionales
## Referencias
