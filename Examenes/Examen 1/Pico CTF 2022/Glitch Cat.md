## Objetivo
Our flag printing service has started glitching! `$ nc saturn.picoctf.net 50363`

## Solución
El puerto nos imprimio la bandera codificada. La ingrese a python3 y la acomode justo para imprimirla como si fuera python obedeciendo el formato y finalmente solto 
```bash
print("picoCTF{gl17ch_m3_n07_" + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}')
picoCTF{gl17ch_m3_n07_a4392d2e}
```

### picoCTF{gl17ch_m3_n07_a4392d2e}
## Notas adicionales
## Referencias
