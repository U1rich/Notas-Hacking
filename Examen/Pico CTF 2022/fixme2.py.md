## Objetivo
Fix the syntax error in the Python script to print the flag.

## Solución
Se abrio el archivo mediante vscode y se modifico la comparaion agregando otre simbolo =
```bash
──(ulrich㉿DasMausoleum)-[~/Descargas]
└─$ python3 fixme2.py
  File "/home/ulrich/Descargas/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/Descargas]
└─$ code fixme2.py 
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/Descargas]
└─$ python3 fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/Descargas]
└─$ 

```

### picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
## Notas adicionales
## Referencias
