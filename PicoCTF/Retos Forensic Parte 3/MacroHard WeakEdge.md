## Description
I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/3944a59474f9f676942282c50b9c3675/Forensics is fun.pptm)

## Hints

## Solution
Como pptm se puede desempaquetar usamos el comando `unzip Forensics\ is\ fun.pptm`
para ver sus archivos.

1. Nos damos cuenta en el desempaquetado que uno dice hidden (Oculto) .
2. Lo busco y lo abro.
3. Hay una cadena de caracteres.
4. Se procede a decodificarlo con cyberchef habiendo borrado espacios.
5. ZmxhZzogcGljb0NURntEMWRfdV9rbjB3X3BwdHNfcl96MXA1fQ
6. Se obiene el resultado ya que era un base64


```bash

  inflating: ppt/tableStyles.xml     
  inflating: docProps/core.xml       
  inflating: docProps/app.xml        
  inflating: ppt/slideMasters/hidden  
```

## Flag
picoCTF{D1d_u_kn0w_ppts_r_z1p5}

## Aditional Notes

## References
