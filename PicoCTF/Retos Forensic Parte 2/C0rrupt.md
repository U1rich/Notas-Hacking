## Description
We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.
## Hints
1. Try fixing the file header

## Solution
Como nos dice que Reparemos el header abrimos el archivo con un editor de texto hexadecimal.
Al observar el hexa podremos apreciar que lon chunks parecen ser de un PNG pero corrompido, por ende deberemos analizarlo mediante pngcheck para ir reparando cada parte.

```bash
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Forensic/c0rrupt]
└─$ pngcheck -v mystery    
File: mystery (202940 bytes)
  File is CORRUPTED.  It seems to have suffered EOL conversion.
ERRORS DETECTED in mystery

(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Forensic/c0rrupt]
└─$ hexedit mystery
89 50 4E 47  0D 0A 1A 0A  00 00 00 0D  .PNG........
0000000C   49 48 44 52  00 00 06 6A  00 00 04 47  IHDR...j...G
00000018   08 02 00 00  00 7C 8B AB  78 00 00 00  .....|..x...
00000024   01 73 52 47  42 00 AE CE  1C E9 00 00  .sRGB.......
00000030   00 04 67 41  4D 41 00 00  B1 8F 0B FC  ..gAMA......
0000003C   61 05 00 00  00 09 70 48  59 73 00 00  a.....pHYs..
00000048   16 25 00 00  16 25 01 49  52 24 F0 00  .%...%.IR$..
00000054   00 FF A5 49  44 41 54 78  5E EC BD 3F  ...IDATx^..?

ahi estan todas las correcciones que se tomaron.

--------------------------
Al ejecutar 
 open mystery
nos aparece el la imagen con la flag

```

## Flag

picoCTF{c0rrupt10n_1847995}

## Aditional Notes

## References
