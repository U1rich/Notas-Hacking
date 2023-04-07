picoCTF{Hiddinng_An_imag3_within_@n_ima9e_cda72af0}

## Objetivo

Every file gets a flag.The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/259/flag.png).
## Hints

## Solución

descargar la imagen y descomprimirla usando el comando unzip, se crea una carpeta nueva dentro hay una imagen con la bandera adentro

```
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico$ identify -verbose flag.png
Image:
  Filename: flag.png
  Format: PNG (Portable Network Graphics)
  Mime type: image/png
  Class: DirectClass
  Geometry: 512x504+0+0
  Units: Undefined
  Colorspace: sRGB
  Type: TrueColorAlpha
  Base type: Undefined
  Endianness: Undefined
  Depth: 8-bit
  Channel depth:
    red: 8-bit
    green: 8-bit
    blue: 8-bit
    alpha: 1-bit
  Channel statistics:
    Pixels: 258048
    Red:
      min: 183  (0.717647)
      max: 255 (1)
      mean: 249.98 (0.980315)
      standard deviation: 16.356 (0.0641413)
      kurtosis: 7.15333
      skewness: -3.01307
      entropy: 0.131488
    Green:
      min: 0  (0)
      max: 255 (1)
      mean: 239.909 (0.940819)
      standard deviation: 52.9864 (0.20779)
      kurtosis: 11.8816
      skewness: -3.61819
      entropy: 0.116298
    Blue:
      min: 0  (0)
      max: 255 (1)
      mean: 242.848 (0.952347)
      standard deviation: 45.092 (0.176831)
      kurtosis: 13.8332
      skewness: -3.89832
      entropy: 0.115899
    Alpha:
      min: 255  (1)
      max: 255 (1)
      mean: 255 (1)
      standard deviation: 0 (0)
      kurtosis: 1.6384e+52
      skewness: 9.375e+35
      entropy: 0
  Image statistics:
    Overall:
      min: 0  (0)
      max: 255 (1)
      mean: 246.934 (0.96837)
      standard deviation: 28.6086 (0.112191)
      kurtosis: 27.4162
      skewness: -5.20888
      entropy: 0.0909213
  Rendering intent: Perceptual
  Gamma: 0.454545
  Chromaticity:
    red primary: (0.64,0.33)
    green primary: (0.3,0.6)
    blue primary: (0.15,0.06)
    white point: (0.3127,0.329)
  Background color: white
  Border color: srgba(223,223,223,1)
  Matte color: grey74
  Transparent color: none
  Interlace: None
  Intensity: Undefined
  Compose: Over
  Page geometry: 512x504+0+0
  Dispose: Undefined
  Iterations: 0
  Compression: Zip <-----
  Orientation: Undefined
  Properties:
    date:create: 2023-03-20T02:22:03+00:00
    date:modify: 2023-03-20T02:22:03+00:00
    png:IHDR.bit-depth-orig: 8
    png:IHDR.bit_depth: 8
    png:IHDR.color-type-orig: 6
    png:IHDR.color_type: 6 (RGBA)
    png:IHDR.interlace_method: 0 (Not interlaced)
    png:IHDR.width,height: 512, 504
    png:sRGB: intent=0 (Perceptual Intent)
    signature: 1681c0af4a3c8c9b12bf3371e2136257cd38225728554db1060c71b9693569d5
  Artifacts:
    filename: flag.png
    verbose: true
  Tainted: False
  Filesize: 42930B
  Number pixels: 258048
  Pixels per second: 34.9507MB
  User time: 0.000u
  Elapsed time: 0:01.007
  Version: ImageMagick 6.9.11-60 Q16 x86_64 2021-01-25 https://imagemagick.org

kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico$ unzip flag.png
Archive:  flag.png
warning [flag.png]:  39739 extra bytes at beginning or within zipfile
  (attempting to process anyway)
replace secret/flag.png? [y]es, [n]o, [A]ll, [N]one, [r]ename: y
  inflating: secret/flag.png
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico$

kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico/secret$ ls
flag.png
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico/secret$
```
### picoCTF{Hiddinng_An_imag3_within_@n_ima9e_cda72af0}

## Notas adicionales
## Referencias
