## Description
A musician left us a [message](https://jupiter.challenges.picoctf.org/static/d5570d48262dbba2a31f2a940409ad9d/message.txt). What's it mean?

## Hints
No hints

## Solution
Me imagine que eran coordenadas pero no pensé que en realidad lo fueran, sin embargo al meterlas a google maps fueron coordenadas exactas.
```bash
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Cripto/Mr-Worldwide]
└─$ cat message.txt 
picoCTF{(35.028309, 135.753082)(46.469391, 30.740883)(39.758949, -84.191605)(41.015137, 28.979530)(24.466667, 54.366669)(3.140853, 101.693207)_(9.005401, 38.763611)(-3.989038, -79.203560)(52.377956, 4.897070)(41.085651, -73.858467)(57.790001, -152.407227)(31.205753, 29.924526)}
```

|Coordenadas | Lugar |
| --------------------- | ---------- |
| 35.028309, 135.753082 | Kyoto, Japon |
| 46.469391, 30.740883 | Odesa, Ukrania |
|39.758949, -84.191605 | Dayton, EU | 
|41.015137, 28.979530 | Estambul, Turquia |
|24.466667, 54.366669| Abu, dhabi |
|3.140853, 101.693207| Kuala, Lampur |
|9.005401, 38.763611|Adis, Abeba|
|-3.989038, -79.203560|Loja, Ecuador|
|52.377956, 4.897070|Amsterdan, Netherlands|
|41.085651, -73.858467| Sleepy Hollow, EU|
|57.790001, -152.407227| Kodiak, EU |
|31.205753, 29.924526| Alexandria, Egipto |

Lo que basicamente queda en KODEAK_ALASKA

## Flag
picoCTF{KODIAK_ALASKA}

## Aditional Notes

## References
