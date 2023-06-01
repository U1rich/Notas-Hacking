## Description
This program has constructed the flag using hex ascii values. Identify the flag text by disassembling the program. You can download the file from [here](https://artifacts.picoctf.net/c/507/asciiftw).

## Hints
1. The combined range of hex-ascii for English alphabets and numerical digits is from 30 to 7A.
2. Online hex-ascii converters can be helpful.

## Solution

```bash
hexedit asciiftw

En el lado ascii de hexedit aparecia un mensaje que decia "la bandera inicia en %" asi que busque porcentajes y me die cuenta de que estaba ese mensaje con basura en medio. Tome el 70 que es la p y lo mande a cyberchef.

								 70  C6 45 D1 69  C6 45 D2 63  E.1..E.p.E.i.E.c
00001190   C6 45 D3 6F  C6 45 D4 43  C6 45 D5 54  C6 45 D6 46  .E.o.E.C.E.T.E.F
000011A0   C6 45 D7 7B  C6 45 D8 41  C6 45 D9 53  C6 45 DA 43  .E.{.E.A.E.S.E.C
000011B0   C6 45 DB 49  C6 45 DC 49  C6 45 DD 5F  C6 45 DE 49  .E.I.E.I.E._.E.I
000011C0   C6 45 DF 53  C6 45 E0 5F  C6 45 E1 45  C6 45 E2 41  .E.S.E._.E.E.E.A
000011D0   C6 45 E3 53  C6 45 E4 59  C6 45 E5 5F  C6 45 E6 37  .E.S.E.Y.E._.E.7
000011E0   C6 45 E7 42  C6 45 E8 43  C6 45 E9 44  C6 45 EA 39  .E.B.E.C.E.D.E.9
000011F0   C6 45 EB 37  C6 45 EC 31  C6 45 ED 44  C6 45 EE 7D

cyberchef

Limpie el mensaje que tenia un patron de c6 45 (D5 - 7D(simbolo de }))

70   69   63
6F   43   54   46  
7B  41  53  43  
49  49   5F  49  
53  5F 45 41
53  59  5F 37
42  43 44 39
37  31 44  7D

ya limpio y convertido de hex a ascii es:

picoCTF{ASCII_IS_EASY_7BCD971D}

```

## Flag
picoCTF{ASCII_IS_EASY_7BCD971D}

## Aditional Notes

## References
