## Description
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag

## Hints
1. Try using a tool like Wireshark.
2. How can you decrypt the TLS stream?

## Solution


```bash
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Forensic]
└─$ cd WebNet0
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Forensic/WebNet0]
└─$ wget https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap && wget https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key
--2023-04-07 01:24:44--  https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap
Resolviendo jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Conectando con jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)[3.131.60.8]:443... conectado.
Petición HTTP enviada, esperando respuesta... 200 OK
Longitud: 13163 (13K) [application/octet-stream]
Grabando a: «capture.pcap»

capture.pcap        100%[===================>]  12.85K  --.-KB/s    en 0s      

2023-04-07 01:24:45 (49.6 MB/s) - «capture.pcap» guardado [13163/13163]

--2023-04-07 01:24:45--  https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key
Resolviendo jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Conectando con jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)[3.131.60.8]:443... conectado.
Petición HTTP enviada, esperando respuesta... 200 OK
Longitud: 1704 (1.7K) [application/octet-stream]
Grabando a: «picopico.key»

picopico.key        100%[===================>]   1.66K  --.-KB/s    en 0s      

2023-04-07 01:24:45 (13.6 MB/s) - «picopico.key» guardado [1704/1704]

                                                                                
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Forensic/WebNet0]
└─$ ls
capture.pcap  picopico.key

e utiliza wireshark capture.pcap
se carga la clave picopico.key en el protocolo tls y se hace una busqueda de strings dentro de los paquetes capturados y ya desencriptados.

```

## Flag
picoCTF{nongshim.shrimp.crackers}

## Aditional Notes

## References
