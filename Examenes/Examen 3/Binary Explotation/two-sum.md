## Description
Can you solve this? What two positive numbers can make this possible: `n1 > n1 + n2 OR n2 > n1 + n2` Enter them here `nc saturn.picoctf.net 56396`. [Source](https://artifacts.picoctf.net/c/455/flag.c)

## Hints
1. Integer overflow
2. Not necessarily a math problem
3. 
## Solution
```bash
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Binary-Explotation]
└─$ code flag.c 
                                                                                   
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Binary-Explotation]
└─$ nc saturn.picoctf.net 56396
n1 > n1 + n2 OR n2 > n1 + n2 
What two positive numbers can make this possible: 
2147483647                                  
1
You entered 2147483647 and 1
You have an integer overflow
YOUR FLAG IS: picoCTF{Tw0_Sum_Integer_Bu773R_0v3rfl0w_fe14e9e9}

```

## Flag
picoCTF{Tw0_Sum_Integer_Bu773R_0v3rfl0w_fe14e9e9}

## Aditional Notes

## References
