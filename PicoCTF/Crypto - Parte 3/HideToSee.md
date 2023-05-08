## Description
How about some hide and seek heh? Look at this image [here](https://artifacts.picoctf.net/c/241/atbash.jpg).

## Hints
Download the image and try to extract it.

## Solution


```bash
┌──(ulrich㉿DasMausoleum)-[~/Descargas]
└─$ steghide extract -sf atbash.jpg
Anotar salvoconducto: 
anot� los datos extra�dos e/"encrypted.txt".
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/Descargas]
└─$ cat encrypted.txt                                            
krxlXGU{zgyzhs_xizxp_7142uwv9}

```
Para decodificar la flag basto con ir a cybechef y buscar el atbash cipher.
## Flag
picoCTF{atbash_crack_7142fde9}

## Aditional Notes

## References
