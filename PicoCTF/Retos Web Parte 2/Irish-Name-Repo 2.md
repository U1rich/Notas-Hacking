## Objetivo
There is a website running at `https://jupiter.challenges.picoctf.org/problem/64649/` ([link](https://jupiter.challenges.picoctf.org/problem/64649/)). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://jupiter.challenges.picoctf.org:64649

## Hints
The password is being filtered.

## Solución

Primero nos damos cuenta de que es la misma pagina que irish1 pero esta captando el sql injection, asi que verificamos como es que se esta evitando el sql injection y al final nos podemos percatar de que las comillas se cierran correctamente con un sqli basico. por ende usamos el nombre:
```sql
admin'; 
```
de esa forma genera una falla e ignora el password, obteniendo el siguiente ctf
### picoCTF{m0R3_SQL_plz_aee925db}
## Notas adicionales
## Referencias
