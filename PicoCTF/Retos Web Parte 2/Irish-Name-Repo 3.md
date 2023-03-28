## Objetivo
There is a secure website running at `https://jupiter.challenges.picoctf.org/problem/54253/` ([link](https://jupiter.challenges.picoctf.org/problem/54253/)) or http://jupiter.challenges.picoctf.org:54253. Try to see if you can login as admin!

## Hints

## Solución
Ahora solo nos pide una contraseña, asi que activams la vulnerabilidad del modo debug y le intoducimos una inyeccion sql, la cual resulta en una solo una contraseña incorecta. Esto sucede porque la contraseña fue codificada primero para evitar que se hagan sentencias con la sintaxis correcta de sql y al ver el resultado lo copiamos y lo pegamos en el passwordpara que aplique de forma inversa la codificacion y nos de como resultado la inyeccion sql.


```sql
password: ' be 1=1;
SQL query: SELECT * FROM admin where password = '' or 1=1;'

# Logged in!

Your flag is: picoCTF{3v3n_m0r3_SQL_7f5767f6}
```

### picoCTF{3v3n_m0r3_SQL_7f5767f6}
## Notas adicionales
## Referencias
