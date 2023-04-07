## Description
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.

## Hints

## Solution
1. Se descargan los paquetes capturados y la llave.
2. Se utiliza wireshark capture.pcap
3. Se carga la clave picopico.key en el protocolo tls y se hace una busqueda de strings dentro de los paquetes capturados y ya desencriptados.
4. Al obtener los resultados de la busueda nos dice que esta no es la flag asi que hacemos un seuimiento de los paquetes desencriptados y finalmente leyendo un poco se logra ver la verdadera FLAG.

```bash

```

## Flag

picoCTF{honey.roasted.peanuts}

## Aditional Notes

## References
