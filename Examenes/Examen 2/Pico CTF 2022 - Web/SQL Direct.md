## Description
Connect to this PostgreSQL server and find the flag!

Additional details will be available after launching your challenge instance.

## Hints
busque la documentacion para postgreSQL, se

## Solution
```sql
pico-# \d
        Listado de relaciones
 Esquema | Nombre | Tipo  |  Dueño   
---------+--------+-------+----------
 public  | flags  | tabla | postgres
(1 fila)

pico=# select * from flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_21c94904}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia


```

## Flag
picoCTF{L3arN_S0m3_5qL_t0d4Y_21c94904}

## Aditional Notes

## References
