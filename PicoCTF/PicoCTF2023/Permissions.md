## Objetivo

Can you read files in the root file? Additional details will be available after launching your challenge instance.

## Hints

## Solución

hay que entrar a al carpeta challenge y revisar el archivo metadatos.json

```
picoplayer@challenge:/$ ls
bin   challenge  etc   lib    lib64   media  opt   root  sbin  sys  usr
boot  dev        home  lib32  libx32  mnt    proc  run   srv   tmp  var
picoplayer@challenge:/$ cd challenge/
picoplayer@challenge:/challenge$ ls
metadata.json
picoplayer@challenge:/challenge$ cat metadata.json
{"flag": "picoCTF{uS1ng_v1m_3dit0r_021d10ab}", "username": "picoplayer", "password": "dLAqMvm7xv"}picoplayer@challenge:/challenge$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico$
```
## picoCTF{uS1ng_v1m_3dit0r_021d10ab}
## Notas adicionales
## Referencias
