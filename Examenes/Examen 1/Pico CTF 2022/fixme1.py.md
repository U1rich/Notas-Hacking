## Objetivo
Fix the syntax error in this Python script to print the flag. [Download Python script](https://artifacts.picoctf.net/c/25/fixme1.py)

## Solución
Se ejecuto el codigo dando como resultado un error  fue solucionado mediante una identacion.

```bash
┌──(ulrich㉿DasMausoleum)-[~/Descargas]
└─$ python3 fixme1.py
  File "/home/ulrich/Descargas/fixme1.py", line 20
    print("That is correct! Here\'s your flag: ", flag)
IndentationError: unexpected indent          
┌──(ulrich㉿DasMausoleum)-[~/Descargas]
└─$ python3 fixme1.py
That is correct! Here's your flag:  picoCTF{1nd3nt1ty_cr1515_6a476c8f}
```

### picoCTF{1nd3nt1ty_cr1515_6a476c8f}

## Notas adicionales
## Referencias
