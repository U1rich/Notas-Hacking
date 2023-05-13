## Description
The name of the game is [speed](https://www.youtube.com/watch?v=8piqd2BWeGI). Are you quick enough to solve this problem and keep it above 50 mph? [need-for-speed](https://jupiter.challenges.picoctf.org/static/cd51b2c95be9f3626db6fe6665afb5a3/need-for-speed).

## Hints
What is the final key?

## Solution
Para la solucion use gdb, puse un breakepoint en main, corri el binario y ejecute directamente el 
```bash
Comandos usados:
chmod +x need-for-speed
gdb need-for-speed
----------gdb-----------
set disassembly-flavor intel
disassemble main
break main
call (int) get_key()
call (int) print_flag()
```

## Flag
PICOCTF{Good job keeping bus #24c43740 speeding along!}

## Aditional Notes

## References
