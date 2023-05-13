## Description
What does asm1(0x6fa) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/b41e08fc19ceb9d0466ebd68d36c5630/test.S)

## Hints
assembly [conditions](https://www.tutorialspoint.com/assembly_programming/assembly_conditions.htm)

## Solution
```asm
Se nos da el parametro 0x6fa
0x6fa
-------------------------------
Stack
0000

[  ebp  ] ebp
[  Ret  ] ebp + 0x4
[ 0x6fa ] ebp + 0x8
FFFF

Registers
eax---> 0x6e8
--------------ASM---------------
asm1:
;Prologo de la funcion
        <+0>:   push   ebp ;crea la pila
        <+1>:   mov    ebp,esp ; apunta esp a la base de la pila


        <+3>:   cmp    DWORD PTR [ebp+0x8],0x3a2 ;Compara 0x3a2 con lo que hay en [memoriaebp+0x8]
                ;La siguiente comparacion es verdadera ya que 0x6fa > 0x3a2 
        <+10>:  jg     0x512 <asm1+37>
        <+12>:  cmp    DWORD PTR [ebp+0x8],0x358 ;Salta a la linea 37 si es mayor la comparacion
        <+19>:  jne    0x50a <asm1+29>
        <+21>:  mov    eax,DWORD PTR [ebp+0x8]
        <+24>:  add    eax,0x12
        <+27>:  jmp    0x529 <asm1+60>
        <+29>:  mov    eax,DWORD PTR [ebp+0x8]
        <+32>:  sub    eax,0x12 
        <+35>:  jmp    0x529 <asm1+60>
        <+37>:  cmp    DWORD PTR [ebp+0x8],0x6fa ;compara el segundo parametro con lo qe hay en buffen nuevamente
                                                 ;y curiosamente es igual entonces el siguiente salto no se activa 
                                                 ;ya que es un "jump if not equal[jne]"
        <+44>:  jne    0x523 <asm1+54> ; se ignora
        <+46>:  mov    eax,DWORD PTR [ebp+0x8] ;mueve el valor que hay en el buffer al regstro eax
        <+49>:  sub    eax,0x12 ; Se le resta 0x12 al registro eax, el resulado es 1768 o 0x6e8.

        <+52>:  jmp    0x529 <asm1+60>  ; Salta incondicionalmente a la linea 60

        <+54>:  mov    eax,DWORD PTR [ebp+0x8]
        <+57>:  add    eax,0x12
        <+60>:  pop    ebp      ; Se trae la pila que generamos y en espesifico el registro
        <+61>:  ret             ; Regresa a donde fue llamado el codigo.

-----------Calculos-------------
>>> 0x6fa > 0x3a2
True
>>> 0x6fa + 0x12
1804
>>> 0x6fa - 0x12
1768
>>> hex(1768)
'0x6e8'
   

```

## Flag
0x6e8

## Aditional Notes
EBP <--- Apuntador de base
ESP <--- Apuntador de pila

## References
