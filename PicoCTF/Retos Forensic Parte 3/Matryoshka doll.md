## Description
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/205adad23bf9d8303081a0e71c9beab8/dolls.jpg)

## Hints
1. Wait, you can hide files inside files? But how do you find them?
2. Make sure to submit the flag as picoCTF{XXXXX}

## Solution

```bash
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Forensic/Matryoshka doll]
└─$ wget https://mercury.picoctf.net/static/205adad23bf9d8303081a0e71c9beab8/dolls.jpg
--2023-04-07 00:16:17--  https://mercury.picoctf.net/static/205adad23bf9d8303081a0e71c9beab8/dolls.jpg
Resolviendo mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Conectando con mercury.picoctf.net (mercury.picoctf.net)[18.189.209.142]:443... conectado.
Petición HTTP enviada, esperando respuesta... 200 OK
Longitud: 651632 (636K) [application/octet-stream]
Grabando a: «dolls.jpg»

dolls.jpg           100%[===================>] 636.36K  1.13MB/s    en 0.6s    

2023-04-07 00:16:18 (1.13 MB/s) - «dolls.jpg» guardado [651632/651632]

                                                                                
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Forensic/Matryoshka doll]
└─$ ls
dolls.jpg
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Forensic/Matryoshka doll]
└─$ binwalk -e dolls.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378952, uncompressed size: 383937, name: base_images/2_c.jpg
651610        0x9F15A         End of Zip archive, footer length: 22

                                                                                
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Forensic/Matryoshka doll]
└─$ ls
dolls.jpg  _dolls.jpg.extracted
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Forensic/Matryoshka doll]
└─$ cd _dolls.jpg.extracted                             
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/…/Apuntes 8vo Semestre/Forensic/Matryoshka doll/_dolls.jpg.extracted]
└─$ ls
4286C.zip  base_images
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/…/Apuntes 8vo Semestre/Forensic/Matryoshka doll/_dolls.jpg.extracted]
└─$ cd base_images         
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/…/Forensic/Matryoshka doll/_dolls.jpg.extracted/base_images]
└─$ ls 
2_c.jpg
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/…/Forensic/Matryoshka doll/_dolls.jpg.extracted/base_images]
└─$ open 2_c.jpg 
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/…/Forensic/Matryoshka doll/_dolls.jpg.extracted/base_images]
└─$ binwalk -e 2_c.jpg  

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 526 x 1106, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
187707        0x2DD3B         Zip archive data, at least v2.0 to extract, compressed size: 196042, uncompressed size: 201444, name: base_images/3_c.jpg
383804        0x5DB3C         End of Zip archive, footer length: 22
383915        0x5DBAB         End of Zip archive, footer length: 22

                                                                                
┌──(ulrich㉿DasMausoleum)-[~/…/Forensic/Matryoshka doll/_dolls.jpg.extracted/base_images]
└─$ cd _2_c.jpg.extracted 
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/…/Matryoshka doll/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted]
└─$ ls                   
2DD3B.zip  base_images
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/…/Matryoshka doll/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted]
└─$ cd base_images       
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ ls
3_c.jpg
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ binwalk -e 3_c.jpg   

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 428 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
123606        0x1E2D6         Zip archive data, at least v2.0 to extract, compressed size: 77650, uncompressed size: 79807, name: base_images/4_c.jpg
201422        0x312CE         End of Zip archive, footer length: 22

                                                                                
┌──(ulrich㉿DasMausoleum)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ cd _3_c.jpg.extracted 
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/…/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted]
└─$ cd base_images       
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ ls
4_c.jpg
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ binwalk -e 4_c.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 320 x 768, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
79578         0x136DA         Zip archive data, at least v2.0 to extract, compressed size: 63, uncompressed size: 81, name: flag.txt
79785         0x137A9         End of Zip archive, footer length: 22

                                                                                
┌──(ulrich㉿DasMausoleum)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ cd _4_c.jpg.extracted 
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/…/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ ls                   
136DA.zip  flag.txt
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/…/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ cat flag.txt         
picoCTF{96fac089316e094d41ea046900197662}                                                                                
┌──(ulrich㉿DasMausoleum)-[~/…/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ 

```

## Flag
picoCTF{96fac089316e094d41ea046900197662}

## Aditional Notes

## References
