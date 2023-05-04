## Description
Can you find the flag? [shark1.pcapng](https://mercury.picoctf.net/static/0505a462ac9beb7412596855df280f6b/shark1.pcapng).

## Hints
none

## Solution

```bash
La solucion se hizo observando las secuencias TCP(eran demaciadas), la que tenia algo parecido a una flag se encontraba en la quinta secuencia. Una vez encontrada  por los corchetes podemos inferir que se trata de un rot13, o el numero que sea, asi que procedemos a decodificarlo en python de la siguiente manera:

>>> import codecs
>>> ctf = 'Gur synt vf cvpbPGS{c33xno00_1_f33_h_qrnqorrs}'
>>> textplane = codecs.decode(ctf,'rot_13')
>>> print(textplane)
                   The flag is picoCTF{p33kab00_1_s33_u_deadbeef}
```

## Flag
picoCTF{p33kab00_1_s33_u_deadbeef}

## Aditional Notes

## References
