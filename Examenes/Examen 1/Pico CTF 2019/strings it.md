## Objetivo
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings) without running it?


## Solución
Si corremos el comando en nuestra consola podremos ver que lanza mucho texto, así que lo que tenemos que hacer ahora es filtrar los resuptados con un grep pico.
```bash
(ulrich㉿DasMausoleum)-[~/Descargas]
└─$ file strings
strings: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=047a5079a5f563cd0e540d28f42a37161093ffda, not stripped
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/Descargas]
└─$ strings strings | grep pico
picoCTF{5tRIng5_1T_827aee91}
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/Descargas]
└─$ 

```

### picoCTF{5tRIng5_1T_827aee91}
## Notas adicionales
## Referencias
