## Description
We found this weird message being passed around on the servers, we think we have a working decryption scheme. Download the message [here](https://artifacts.picoctf.net/c/127/message.txt). Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore. Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)

## Hints
1. Do you know what `mod 37` means?
2. `mod 37` means modulo 37. It gives the remainder of a number after being divided by 37.

## Solution


```bash
-------Se creo un codigo .py------
data  = open('message.txt').read().strip().split()
flag = ''
for n in data:
	n = int(n) % 37
	if n>=0 and n<=25:
		c = chr(n+65)
	elif n>=26 and n<=35:
		c = chr(n+22)
	else :
		c = '_'
	flag += c

print(flag)
(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Cripto/basic-Mod1]
└─$ nano mod37.py   
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Cripto/basic-Mod1]
└─$ python3 mod37.py
R0UND_N_R0UND_79C18FB3
```

## Flag
picoCTF{R0UND_N_R0UND_79C18FB3}
## Aditional Notes

## References
