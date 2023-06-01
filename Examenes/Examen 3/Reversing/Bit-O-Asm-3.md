## Description
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`. Download the assembly dump [here](https://artifacts.picoctf.net/c/530/disassembler-dump0_c.txt).

## Hints
Not everything in this disassembly listing is optimal.

## Solution
```bash
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Reversing]
└─$ cat disassembler-dump0_c.txt 
<+0>:     endbr64 
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x14],edi
<+11>:    mov    QWORD PTR [rbp-0x20],rsi
<+15>:    mov    DWORD PTR [rbp-0xc],0x9fe1a -- Mueve a memoria 0x9fe1a
<+22>:    mov    DWORD PTR [rbp-0x8],0x4     -- Mueve a memoria 0x4 
<+29>:    mov    eax,DWORD PTR [rbp-0xc]     -- Carga en eax lo que hay en dir c
<+32>:    imul   eax,DWORD PTR [rbp-0x8]     -- Multiplica lo que hay en eax con lo qe hay en dir 8 y lo guarda en eax
<+36>:    add    eax,0x1f5                   -- Suma a eax esto 0x1f5
<+41>:    mov    DWORD PTR [rbp-0x4],eax     -- Guarda en la direccion 0x4 el contenido de eax
<+44>:    mov    eax,DWORD PTR [rbp-0x4]     -- Saca de 0x4 y lo pone en eax
<+47>:    pop    rbp
<+48>:    ret

(0x9fe1a)(0x4)+(0x1f5) = 0x27FA5D = d2619997
```

## Flag
picoCTF{2619997}

## Aditional Notes

## References
