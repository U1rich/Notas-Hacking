## Descripción

Help us test the form by submiting the username as `test` and password as `test!` The website running [here](http://saturn.picoctf.net:54319/).

## Hints

any redirections?

## Solución

Al ir a la página nos encontramos con un formulario que pide usuario y contraseña. Al introducir las credenciales que nos sugiere la descripción del reto, nos mandan a la página `/home` donde aparentemente podemos buscar banderas. Al inspeccionar el código fuente, nos damos cuenta que es una mentira y en la página /home no hay nada útil, solamente simula que podemos buscar banderas con el cuadro de texto. Al navegar una página hacia atrás, nos damos cuenta que hemos sido redirigidos 2 veces, primero al URL `http://saturn.picoctf.net:54319/next-page/id=cGljb0NURntwcm94aWVzX2Fs` y después al URL `http://saturn.picoctf.net:54319/next-page/id=bF90aGVfd2F5XzAxZTc0OGRifQ==`. Como el titulo de las páginas en estos URL es "flag", probablemente significa que la parte de `id=` forma parte de la bandera.

Al introducir ambas partes directamente al formato de bandera picoCTF{} resulta que no es una bandera válida; asumimos que hay que desencriptar primero.

Introducimos la primera parte `cGljb0NURntwcm94aWVzX2Fs` a la herramienta CyberChef y nos sugiere que el texto está encriptado en base 64.

`cGljb0NURntwcm94aWVzX2FsbF90aGVfd2F5XzAxZTc0OGRifQ==` -> `picoCTF{proxies_all_the_way_01e748db}`

## Bandera

```
picoCTF{proxies_all_the_way_01e748db}
```

## Notas adicionales

## Referencias

[Solución en CyberChef](https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Y0dsamIwTlVSbnR3Y205NGFXVnpYMkZzYkY5MGFHVmZkMkY1WHpBeFpUYzBPR1JpZlE9PQ)