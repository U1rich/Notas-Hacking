## Description
What can you do with this file? I forgot the key to my safe but this [file](https://artifacts.picoctf.net/c/286/SafeOpener.class) is supposed to help me with retrieving the lost key. Can you help me unlock my safe?

## Hints
Download and try to decompile the file.

## Solution
Utilice ghidra para decompilar el compilado java, basto importar el programa y ejecutar ghidra.

```c++
/* Flags:
     ACC_PUBLIC
     ACC_STATIC
   
   public static boolean openSafe(String password)  */

boolean openSafe_java.lang.String_boolean(String param1)

{
  PrintStream pPVar1;
  boolean bVar2;
  
  bVar2 = param1.equals("picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_3dae8463}");
  if (bVar2 != false) {
    pPVar1 = System.out;
    pPVar1.println("Sesame open");
    return true;
  }
  pPVar1 = System.out;
  pPVar1.println("Password is incorrect\n");
  return false;
}
```

## Flag
picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_3dae8463}

## Aditional Notes

## References
