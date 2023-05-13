## Description
What does asm2(0x4,0x21) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/7e3eb2f90200ac88126f62ceb4bc3948/test.S)

## Hints
assembly [conditions](https://www.tutorialspoint.com/assembly_programming/assembly_conditions.htm)

## Solution


```asm

--------PILA---------     
0x4,0x21

Stack
[0000]
[    ]< [esp]
[    ] ebp -16
[0x4 ] ebp -8
[0x21] ebp -4
[ebp ]  
[ret ] ebp +4
[0x4 ] ebp +8
[0x21] ebp +c
[FFFF]
'0x24c'
Registros 
EAX = 0x21
EAX = 0x24c ULTIMO EAX

---------ASM2---------
asm2: ; Esta funcion fue invocada con dos parametros 0x4,0x21

        <+0>:   push   ebp ;  marca la base de la pila
        <+1>:   mov    ebp,esp ;  marca la base y el apuntador de la pila
        <+3>:   sub    esp,0x10 ; movemos al apuntador [esp] en 0x10 o 16 bits. 
        <+6>:   mov    eax,DWORD PTR [ebp+0xc] ; movemos lo que hay en ebp + 12 a eax
        <+9>:   mov    DWORD PTR [ebp-0x4],eax ; Mueve lo que hay en eax a la direccion ebp-0x4
        <+12>:  mov    eax,DWORD PTR [ebp+0x8] ; Mueve lo que hay en ebp+ 0x8 al registro eax
        <+15>:  mov    DWORD PTR [ebp-0x8],eax ; mueve lo que hay en eax a la direccion ebp-0x8
        <+18>:  jmp    0x509 <asm2+28> ; salto incondicional a la linea 28
        <+20>:  add    DWORD PTR [ebp-0x4],0x1 ; Le suma al valor de  esta direccion que tiene el hex 0x21 un +1
        <+24>:  add    DWORD PTR [ebp-0x8],0x74 ; Le suma al valor de esta direccion +74
        <+28>:  cmp    DWORD PTR [ebp-0x8],0xfb46 ; compara lo que hay en la direccion ebp-0x8 con 0xfb46
        <+35>:  jle    0x501 <asm2+20> ; Si es menor o igual salta a la 20  por lo tanto salta 
                                        ; 
        <+37>:  mov    eax,DWORD PTR [ebp-0x4] ; 
        <+40>:  leave  
        <+41>:  ret   
---------PYTHON-------
>>> 0xfb46 / 0x74
554.5344827586207
>>> int(0x21)
33
>>> hex(33+555)
'0x24c'

```

## Flag
0x24c
## Aditional Notes

## References
