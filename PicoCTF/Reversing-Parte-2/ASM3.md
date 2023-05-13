## Description
What does asm3(0xd2c26416,0xe6cf51f0,0xe54409d5) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/df999527eaecf46f259c4337a820856c/test.S)

## Hints

## Solution
Use un emulador porque los registros estaban toando cahitos y me perdia muy facilmente al hacerlo manualmente.

```asm
start:
    push 0xe54409d5
    push 0xe6cf51f0
    push 0xd2c26416
    call asm3

asm3: ; nos dan  0xd2c26416,0xe6cf51f0,0xe54409d5 como argumentos

        push   ebp
        mov    ebp,esp

        xor    eax,eax ;Limpia el registro eax
        mov    ah,BYTE PTR [ebp+0x9]
        shl    ax,0x10
        sub    al,BYTE PTR [ebp+0xe]
        add    ah,BYTE PTR [ebp+0xf]
        xor    ax,WORD PTR [ebp+0x12]
        nop
        pop    ebp
        ret  

```

## Flag
0x375
## Aditional Notes
For optimization purposes (it only requires 2 bytes), the xor instruction is often used that way to clear the value of a register: `EOR EAX,EAX`
Emulador: https://carlosrafaelgn.com.br/Asm86/

## References
