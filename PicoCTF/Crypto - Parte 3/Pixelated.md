## Description
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/9f2d081f12c05202359632c1989e7927/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/9f2d081f12c05202359632c1989e7927/scrambled2.png)

## Hints
1. Think of different ways you can "stack" images.
2. [https://en.wikipedia.org/wiki/Visual_cryptography](https://en.wikipedia.org/wiki/Visual_cryptography)


## Solution


```bash
wget https://mercury.picoctf.net/static/9f2d081f12c05202359632c1989e7927/scrambled2.png 
--2023-04-27 08:46:00--  https://mercury.picoctf.net/static/9f2d081f12c05202359632c1989e7927/scrambled2.png
Resolviendo mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Conectando con mercury.picoctf.net (mercury.picoctf.net)[18.189.209.142]:443... conectado.
Petición HTTP enviada, esperando respuesta... 200 OK
Longitud: 197173 (193K) [application/octet-stream]
Grabando a: «scrambled2.png»

scrambled2.png       100%[=====================>] 192.55K   232KB/s    en 0.8s    

2023-04-27 08:46:10 (232 KB/s) - «scrambled2.png» guardado [197173/197173

┌──(ulrich㉿DasMausoleum)-[~/Descargas]
└─$ convert scrambled1.png scrambled2.png -compose add -composite flag.png
                                                                                   
┌──(ulrich㉿DasMausoleum)-[~/Descargas]
└─$ open flag.png 

```

## Flag
picoCTF{7188864c}

## Aditional Notes

## References
