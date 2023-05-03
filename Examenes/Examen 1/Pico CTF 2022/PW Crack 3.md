## Objetivo
Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/18/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/18/level3.hash.bin) in the same directory too. There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

## Solución
Abri el programa y me di cuenta de que habia una lista de pocas contraseñas, pense en meterlas a una ista y hacer una prueba automatica pero cmo eran pocas simplemente las cope y pegue en el programa.
```bash
─(ulrich㉿DasMausoleum)-[~/Descargas]
└─$ python3 level3.py
Please enter correct password for flag: acaf
That password is incorrect
                                                                                   
┌──(ulrich㉿DasMausoleum)-[~/Descargas]
└─$ python3 level3.py
Please enter correct password for flag: 2295
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_6f98a49f}
```

### picoCTF{}
## Notas adicionales
## Referencias
