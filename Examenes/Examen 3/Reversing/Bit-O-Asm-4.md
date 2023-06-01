## Description
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`. Download the assembly dump [here](https://artifacts.picoctf.net/c/511/disassembler-dump0_d.txt).

## Hints
1. Don't tell anyone I told you this, but you can solve this problem without understanding the compare/jump relationship.
2. Of course, if you're really good, you'll only need one attempt to solve this problem.

## Solution
```bash
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Reversing]
└─$ wget https://artifacts.picoctf.net/c/511/disassembler-dump0_d.txt && cat disassembler-dump0_d.txt
--2023-05-31 20:32:52--  https://artifacts.picoctf.net/c/511/disassembler-dump0_d.txt
Resolviendo artifacts.picoctf.net (artifacts.picoctf.net)... 2600:9000:24da:b600:16:5ec5:2840:93a1, 2600:9000:24da:ea00:16:5ec5:2840:93a1, 2600:9000:24da:c800:16:5ec5:2840:93a1, ...
Conectando con artifacts.picoctf.net (artifacts.picoctf.net)[2600:9000:24da:b600:16:5ec5:2840:93a1]:443... conectado.
Petición HTTP enviada, esperando respuesta... 200 OK
Longitud: 482 [application/octet-stream]
Grabando a: «disassembler-dump0_d.txt»

disassembler-dump0_d 100%[=====================>]     482  --.-KB/s    en 0s      

2023-05-31 20:32:53 (3.98 MB/s) - «disassembler-dump0_d.txt» guardado [482/482]

<+0>:     endbr64 
<+4>:     push   rbp 
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x14],edi
<+11>:    mov    QWORD PTR [rbp-0x20],rsi
<+15>:    mov    DWORD PTR [rbp-0x4],0x9fe1a
<+22>:    cmp    DWORD PTR [rbp-0x4],0x2710
<+29>:    jle    0x55555555514e <main+37> - Salta si es menor o igual
<+31>:    sub    DWORD PTR [rbp-0x4],0x65 - resta 65 a lo que ha en la direccion 0x4
<+35>:    jmp    0x555555555152 <main+41> - salta a la instruccion 41
<+37>:    add    DWORD PTR [rbp-0x4],0x65 
<+41>:    mov    eax,DWORD PTR [rbp-0x4]  - guarda en eax lo que hay en la direccion 0x4
<+44>:    pop    rbp
<+45>:    ret

eax = (9FE1A−65) = 0x9FDB5 = d654773
```

## Flag
picoCTF{654773}

## Aditional Notes

## References
