## Description
Decode this [message](https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav) from the moon.

## Hints
1. How did pictures from the moon landing get sent back to Earth?
2. What is the CMU mascot?, that might help select a RX option
## Solución

Instalamos sstv
Ejecutamos 

```bash
──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Forensic/m00nwalk]
└─$ sudo apt install qsstv 
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Forensic/m00nwalk]
└─$ sstv -d message.wav -o response.png               
[sstv] Searching for calibration header... Found!    
[sstv] Detected SSTV mode Scottie 1
[sstv] Decoding image...   [##############################################] 100%
[sstv] Drawing image data...
[sstv] ...Done!
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Forensic/m00nwalk]
└─$ open response.png 

```

### picoCTF{beep_boop_im_in_space}
## Notas adicionales
## Referencias
