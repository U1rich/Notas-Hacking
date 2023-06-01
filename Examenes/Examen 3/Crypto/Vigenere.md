## Description
Can you decrypt this message? Decrypt this [message](https://artifacts.picoctf.net/c/158/cipher.txt) using this key "CYLAB".

## Hints
https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher

## Solution
Se nos dio una clave y una key para usarla como vigenere por lo tanto, usamos cyberchef y de esa forma fácilmente da la solución.

```bash
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Cripto]
└─$ file cipher.txt      
cipher.txt: ASCII text
                                                                                   
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Cripto]
└─$ strings cipher.txt         
rgnoDVD{O0NU_WQ3_G1G3O3T3_A1AH3S_cc82272b}

```

## Flag
picoCTF{D0NT_US3_V1G3N3R3_C1PH3R_ae82272q}

## Aditional Notes

## References
