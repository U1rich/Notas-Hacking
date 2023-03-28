## Objetivo
There is some interesting information hidden around this site [http://mercury.picoctf.net:27393/](http://mercury.picoctf.net:27393/). Can you find it?

## Solución
Basicamente hay que verificar la pagina mediante el inspector para encontrar en los comentarios las diferentes partes de la bandera. La primera se encuentra apenas entrando al inspector

```html
Se encuentra en index.html
picoCTF{t

Esta se encuentra en los CSS
h4ts_4_l0

La siguiente la encontre en robots.txt
t_0f_pl4c

Esta como nos decia que era un servidor apache verificamos el .htaccess
3s_2_lO0k

Finalmente como nos menciono que era una MAC y la palabra clave store se relaciono con el .DS_Store
_d375c750}
```

### picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_d375c750}
## Notas adicionales
## Referencias
