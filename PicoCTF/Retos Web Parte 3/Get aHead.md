## Objetivo
Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:15931/](http://mercury.picoctf.net:15931/)


## Solución
se envio mediante el comando curl el encabezado --head para recibir la respuesta correcta

```bash
curl --head http://mercury.picoctf.net:15931/index.php
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_82880908}
Content-type: text/html; charset=UTF-8
```

### picoCTF{r3j3ct_th3_du4l1ty_82880908}
## Notas adicionales
## Referencias
