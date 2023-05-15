## Description
Intentar decifrar esta cosa

## Hints
None

## Solution
Como es un archivo .java lo abrí y me di cuenta que la linea de la flag estaba codificada en base64, por lo que hice un script que le diera donde mas le duele "la decodificacion".

```python
>>>import base64
>>>code = 'cGwzYXMzX2wzdF9tM18xbnQwX3RoM19zYWYz'
>>> flag = base64.b64decode(code)
b'pl3as3_l3t_m3_1nt0_th3_saf3'
>>>print("picoCTF{"+str(flag)+"}")
picoCTF{b'pl3as3_l3t_m3_1nt0_th3_saf3'}
En esta parte solo se le quita las comillas y la b al principio y listo, queda la flag.
```

## Flag
picoCTF{pl3as3_l3t_m3_1nt0_th3_saf3}

## Aditional Notes

## References
