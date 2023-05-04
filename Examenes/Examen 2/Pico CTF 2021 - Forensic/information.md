## Description
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/c28a959c5605d5f67480d5dd3a77f302/cat.jpg)
## Hints
1. Look at the details of the file.
2. Make sure to submit the flag as picoCTF{XXXXX}

## Solution


```bash
00000000   FF D8 FF E0  00 10 4A 46  49 46 00 01  02 00 00 01  00 01 00 00  FF ED 00 30  50 68 6F 74  6F 73 68 6F  70 20 33 2E  ......JFIF.............0Photoshop 3.
00000024   30 00 38 42  49 4D 04 04  00 00 00 00  00 13 1C 02  74 00 07 50  69 63 6F 43  54 46 1C 02  00 00 02 00  04 00 FF E1  0.8BIM..........t..PicoCTF..........
00000048   0B F9 68 74  74 70 3A 2F  2F 6E 73 2E  61 64 6F 62  65 2E 63 6F  6D 2F 78 61  70 2F 31 2E  30 2F 00 3C  3F 78 70 61  ..http://ns.adobe.com/xap/1.0/.<?xpa
0000006C   63 6B 65 74  20 62 65 67  69 6E 3D 27  EF BB BF 27  20 69 64 3D  27 57 35 4D  30 4D 70 43  65 68 69 48  7A 72 65 53  cket begin='...' id='W5M0MpCehiHzreS
00000090   7A 4E 54 63  7A 6B 63 39  64 27 3F 3E  0A 3C 78 3A  78 6D 70 6D  65 74 61 20  78 6D 6C 6E  73 3A 78 3D  27 61 64 6F  zNTczkc9d'?>.<x:xmpmeta xmlns:x='ado
000000B4   62 65 3A 6E  73 3A 6D 65  74 61 2F 27  20 78 3A 78  6D 70 74 6B  3D 27 49 6D  61 67 65 3A  3A 45 78 69  66 54 6F 6F  be:ns:meta/' x:xmptk='Image::ExifToo
000000D8   6C 20 31 30  2E 38 30 27  3E 0A 3C 72  64 66 3A 52  44 46 20 78  6D 6C 6E 73  3A 72 64 66  3D 27 68 74  74 70 3A 2F  l 10.80'>.<rdf:RDF xmlns:rdf='http:/
000000FC   2F 77 77 77  2E 77 33 2E  6F 72 67 2F  31 39 39 39  2F 30 32 2F  32 32 2D 72  64 66 2D 73  79 6E 74 61  78 2D 6E 73  /www.w3.org/1999/02/22-rdf-syntax-ns
00000120   23 27 3E 0A  0A 20 3C 72  64 66 3A 44  65 73 63 72  69 70 74 69  6F 6E 20 72  64 66 3A 61  62 6F 75 74  3D 27 27 0A  #'>.. <rdf:Description rdf:about=''.
00000144   20 20 78 6D  6C 6E 73 3A  63 63 3D 27  68 74 74 70  3A 2F 2F 63  72 65 61 74  69 76 65 63  6F 6D 6D 6F  6E 73 2E 6F    xmlns:cc='http://creativecommons.o
00000168   72 67 2F 6E  73 23 27 3E  0A 20 20 3C  63 63 3A 6C  69 63 65 6E  73 65 20 72  64 66 3A 72  65 73 6F 75  72 63 65 3D  rg/ns#'>.  <cc:license rdf:resource=
0000018C   27 63 47 6C  6A 62 30 4E  55 52 6E 74  30 61 47 56  66 62 54 4E  30 59 57 52  68 64 47 46  66 4D 58 4E  66 62 57 39  'cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9
000001B0   6B 61 57 5A  70 5A 57 52  39 27 2F 3E  0A 20 3C 2F  72 64 66 3A  44 65 73 63  72 69 70 74  69 6F 6E 3E  0A 0A 20 3C  kaWZpZWR9'/>. </rdf:Description>.. <
000001D4   72 64 66 3A  44 65 73 63  72 69 70 74  69 6F 6E 20  72 64 66 3A  61 62 6F 75  74 3D 27 27  0A 20 20 78  6D 6C 6E 73  rdf:Description rdf:about=''.  xmlns
000001F8   3A 64 63 3D  27 68 74 74  70 3A 2F 2F  70 75 72 6C  2E 6F 72 67  2F 64 63 2F  65 6C 65 6D  65 6E 74 73  2F 31 2E 31  :dc='http://purl.org/dc/elements/1.1
0000021C   2F 27 3E 0A  20 20 3C 64  63 3A 72 69  67 68 74 73  3E 0A 20 20  20 3C 72 64  66 3A 41 6C  74 3E 0A 20  20 20 20 3C  /'>.  <dc:rights>.   <rdf:Alt>.    <
00000240   72 64 66 3A  6C 69 20 78  6D 6C 3A 6C  61 6E 67 3D  27 78 2D 64  65 66 61 75  6C 74 27 3E  50 69 63 6F  43 54 46 3C  rdf:li xml:lang='x-default'>PicoCTF<
00000264   2F 72 64 66  3A 6C 69 3E  0A 20 20 20  3C 2F 72 64  66 3A 41 6C  74 3E 0A 20  20 3C 2F 64  63 3A 72 69  67 68 74 73  /rdf:li>.   </rdf:Alt>.  </dc:rights
00000288   3E 0A 20 3C  2F 72 64 66  3A 44 65 73  63 72 69 70  74 69 6F 6E  3E 0A 3C 2F  72 64 66 3A  52 44 46 3E  0A 3C 2F 78  >. </rdf:Description>.</rdf:RDF>.</x
000002AC   3A 78 6D 70  6D 65 74 61  3E 0A 20 20  20 20 20 20  20 20 20 20  20 20 20 20  20 20 20 20  20 20 20 20  20 20 20 20  :xmpmeta>.

Aqui aparecio un par de codigos en bases64(curioso)

W5M0MpCehiHzreSzNTczkc9d <--- Este no dio nada congruente

cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9 <-- Este dio la FLAG

┌──(ulrich㉿DasMausoleum)-[~/…/Apuntes 8vo Semestre/Forensic/Examen-2/information]
└─$ echo cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9 | base64 -d
    picoCTF{the_m3tadata_1s_modified}
```

## Flag
picoCTF{the_m3tadata_1s_modified}

## Aditional Notes

## References
