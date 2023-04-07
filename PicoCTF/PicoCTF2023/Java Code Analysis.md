## Descripción

BookShelf Pico, my premium online book-reading service. I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book! Here are the credentials to get you started:

-   Username: "user"
-   Password: "user"

Source code can be downloaded [here](https://artifacts.picoctf.net/c/478/bookshelf-pico.zip). Website can be accessed [here!](http://saturn.picoctf.net:49754/).

## Hints

1.  Maybe try to find the JWT Signing Key ("secret key") in the source code? Maybe it's hardcoded somewhere? Or maybe try to crack it?
2.  The 'role' and 'userId' fields in the JWT can be of interest to you!
3.  The 'controllers', 'services' and 'security' java packages in the given source code might need your attention. We've provided a README.md file that contains some documentation.
4.  Upgrade your 'role' with the _new_ (cracked) JWT. And re-login for the new role to get reflected in browser's localStorage.

## Solución

De antemano sabemos que es un servicio de lectura de e-books. Podemos loggearnos con el usuario y contraseña proveídos en la descripción del reto. Podemos observar 3 libros, uno de ellos llamado "FLAG" el cual aparentemente está solo disponible para el Admin. ![[Pasted image 20230319145024.png|300]]

Al dar click se nos niega el acceso y nos dicen que debemos tener el **rol Admin** para tener acceso a la bandera.

Nos dan muchas pistas útiles:

-   Se están utilizando tokens JWT para inicio de sesión
-   Los campos importantes en el token son "role" y "userid"
-   La palabra clave para los tokens JWT se encuentra en el código fuente, posiblemente hardcodeado
-   Objetivo: debemos crear nuestro propio token JWT de alguna manera

Al ejecutar una búsqueda en archivos del código fuente con la palabra "jwt" nos encontramos con la clase `JwtService`. En su constructor tiene la variable `secretGenerator` como argumento, del tipo `SecretGenerator`, del cual llama al método `getServerSecret()`

```
	public JwtService(SecretGenerator secretGenerator){
		this.SECRET_KEY = secretGenerator.getServerSecret();
	}
```

Si vamos a la definición de dicha clase, nos damos cuenta que la función de generar una cadena aleatoria en realidad no es aleatoria:

```
    private String generateRandomString(int len) {
        // not so random
        return "1234";
    }
```

Y dado que ésta función se usa como palabra clave del token JWT:

```
String getServerSecret() {
	...
	String newSecret = generateRandomString(32);
	...
	return newSecret;
}
```

Ahora podemos crear nuestro propio token JWT con los campos que queramos. Abrimos las herramientas de desarrollador del navegador y vamos a la pestaña de almacenamiento. Abrimos la sección de Almacenamiento local para extraer el token JWT (auth-token) y lo introducimos a la herramienta de [https://jwt.io/](https://jwt.io/).

Nos dijeron cuáles campos son los importantes, pero no sabemos qué valores serían válidos. Analizamos el código fuente y nos encontramos con el archivo `\bookshelf-pico\src\main\resources\data.sql`, el cual contiene los roles existentes. Escribimos "Admin" en el campo `role`.

Aunque inicialmente creí que `userId` representaba el valor numérico del rol, en realidad probablemente no tiene nada que ver con que el valor numérico del rol Admin sea 4.

![[Pasted image 20230319154011.png]]

Copiamos este nuevo token al Almacenamiento local y también cambiamos el valor de `token-payload` para que coincida con el nuevo rol de Admin. ![[Pasted image 20230319154034.png]]

Refrescamos la página y parece que ya somos Admin. Notamos que Intentar ver el libro `flag,pdf` arroja un error. Si entramos al perfil podemos ver que seguimos en la cuenta de user. Entramos al dashboard en la parte superior derecha y podemos ver que tenemos acceso a la lista de libros y de usuarios.

No podemos modificar el rol del usuario `user`, pero con esta nueva información podemos crear un nuevo token que contenga en los campos userId = 2 y email = admin. Introducimos el nuevo token al almacenamiento local del navegador y refrescamos la página. Si revisamos el perfil podemos ver que ahora estamos en la cuenta de admin.

Vamos al inicio de la página a intentar ver el libro `flag.pdf` y obtenemos la bandera.

## [](https://github.com/KIFUEL/Notas_bandit/blob/main/Pico%20ctf%202023/Java%20Code%20Analysis.md#bandera)

## Bandera

```
picoCTF{w34k_jwt_n0t_g00d_602ce414}
```
