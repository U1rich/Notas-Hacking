## Description
We found this [file](https://mercury.picoctf.net/static/09a86202e72dbdb5bf4d1b5d2c6a5b86/tunn3l_v1s10n). Recover the flag.

## Hints
Weird that it won't display right...

## Solution
1. Revisamos el archivo
2. usamos `xxd` para identificar el tipo de arhivo
3. Al darnos cuenta de que el encabezado es BM cambiamos la extencion a .bmp pero sin embargo no se abre, dice que tamaño del encabezado no soportado.
4.  Cambiamos al tamaño del encabezado para windows que es 28 hex.
5. Address --> 0E
6. BA D0 a 28 00
7. Y donde empiezan los datos
8. Address --> 0A
9. BA D0 a 28 00
10. Pero al guardar y abrir nos da una bandera falsa. Tendremos que buscar la bandera en toda la imagen por ende se ampliara por completo agregando altura al address 16

```bash

```

## Flag

picoCTF{qu1t3_a_v13w_2020}

## Aditional Notes

## References
