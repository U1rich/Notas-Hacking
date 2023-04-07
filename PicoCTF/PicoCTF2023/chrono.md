## Descripción

How to automate tasks to run at intervals on linux servers? Use ssh to connect to this server:

```
Server: saturn.picoctf.net
Port: 61741
Username: picoplayer 
Password: a-8nJGZCTa
```

## Hints

## Solución

Ir a la carpeta /etc/ y buscar archivos que tengan que ver con `cron`.

```
picoplayer@challenge:~$ cd /etc/ 
picoplayer@challenge:/etc$ ls -la | grep cron
drwxr-xr-x 1 root   root       26 Mar 16 02:00 cron.d
drwxr-xr-x 1 root   root       26 Mar 16 02:00 cron.daily
drwxr-xr-x 2 root   root       26 Mar 16 02:00 cron.hourly
drwxr-xr-x 2 root   root       26 Mar 16 02:00 cron.monthly
drwxr-xr-x 2 root   root       26 Mar 16 02:00 cron.weekly
-rw-r--r-- 1 root   root       43 Mar 16 02:01 crontab
picoplayer@challenge:/etc$ cd crontab 
-bash: cd: crontab: Not a directory
picoplayer@challenge:/etc$ file crontab 
crontab: ASCII text
picoplayer@challenge:/etc$ cat crontab 
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_7754e199}
```

## Bandera

```
picoCTF{Sch3DUL7NG_T45K3_L1NUX_7754e199}
```

## Notas adiccionales
## Referencias
