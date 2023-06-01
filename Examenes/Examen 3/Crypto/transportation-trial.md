## Description
Our data got corrupted on the way here. Luckily, nothing got replaced, but every block of 3 got scrambled around! The first word seems to be three letters long, maybe you can use that to recover the rest of the message. Download the corrupted message [here](https://artifacts.picoctf.net/c/193/message.txt).

## Hints

## Solution
Cada 3 letras se cambio, asi que se reorganiza una vez mas mediante código.

```bash
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Cripto]
└─$ cat message.txt                                    
heTfl g as iicpCTo{7F4NRP051N5_16_35P3X51N3_V9AAB1F8}7

┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Cripto]
└─$ code transpototion-trial.py                
                                                                                   
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Cripto]
└─$ python3 transpototion-trial.py 
picoCTF{7R4N5P051N6_15_3XP3N51V3_A9AFB178}
```
```python
#Se uso el sguiente codigo:
flag_enc = "heTfl g as iicpCTo{7F4NRP051N5_16_35P3X51N3_V9AAB1F8}7"

flag = ""

for i in range(12, len(flag_enc),3):

	temp = flag_enc[i:i+3]

	flag += temp[2] + temp[0:2]

print(flag)

```

## Flag
picoCTF{7R4N5P051N6_15_3XP3N51V3_A9AFB178}

## Aditional Notes

## References
