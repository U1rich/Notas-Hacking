## Objetivo
Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/12/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/12/level1.flag.txt.enc) in the same directory too.

## Solución
En este pograma solo era necesario observar el codigo fuente y y observar una comparacion de contraseña. Al ejecutar el codigo se agrego la contraseña que comparaba y se decodifico el contenido del otro archivo.
```bash
──(ulrich㉿DasMausoleum)-[~/Descargas]
└─$ code level1.py 
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/Descargas]
└─$ python3 level1.py 
Please enter correct password for flag: 8713
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_1b2fd683}
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/Descargas]

```

### picoCTF{545h_r1ng1ng_1b2fd683}
## Notas adicionales
## Referencias
