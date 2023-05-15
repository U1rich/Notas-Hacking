## Description
We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/31c9b832d036a10daeef52d8b4290ef0/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/31c9b832d036a10daeef52d8b4290ef0/rev_this). Can you reverse the flag.

## Hints

## Solution
```bash
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Reversing/Reverse_Cipher]
└─$ nano decripter.py   
                                                                                   
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Reversing/Reverse_Cipher]
└─$ python3 decripter.py
picoCTF{r3v3rs37ee84d27}
```
Se utilizo el siguiente script en python para desencriptar una vez habiendo analizndo el binaio mediante  **ghidra 
```python
cifrado= open('rev_this','r').read()

flag= ''
for i in range(8,len(cifrado)-1):
        if i & 1 == 0:
                flag += chr( ord(cifrado[i]) - 5)
        else:
                flag += chr( ord(cifrado[i]) + 2)

print("picoCTF{"+flag+"}")

```
## Flag
picoCTF{r3v3rs37ee84d27}

## Aditional Notes

## References
