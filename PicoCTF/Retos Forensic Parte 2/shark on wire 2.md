## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.

## Solución
Usando wire shark nos damos cuenta de que existen varios packetes que tienen numeros arriba de 5000, algo totalmente raro ya que empiezan desde que se puede leer "start" y finalizan en "end".
Se verifica que es codigo ASCII al restar los 5000 al numero total y como son muchas letras lo automatizamos con un codigo en python:

```python
from scapy.all import *

packets = rdpcap('capture.pcap')

flag = ''

for p in packets:
if UDP in p and p[UDP].dport == 22:
if p[UDP].sport > 5000:
flag += chr(p[UDP].sport - 5000)

print(flag)


┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Forensic/Sharkthewire]
└─$ python3 scrapy.py 
picoCTF{p1LLf3r3d_data_v1a_st3g0}
                                                                                
┌──(ulrich㉿DasMausoleum)-[~/Documentos/Apuntes 8vo Semestre/Forensic/Sharkthewire]
└─$ 



```

### picoCTF{p1LLf3r3d_data_v1a_st3g0}
## Notas adicionales
`sudo apt install python3-scapy`
## Referencias
