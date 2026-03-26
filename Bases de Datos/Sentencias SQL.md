
## Iniciar el entorno

En este texto se van a trabajar con bases de datos relacionales, dicho esto vamos a mencionar unas cosas a tener en cuenta antes de preparar el entorno y empezar hacer nuestros primeros acercamientos en la gestión de bases de datos.

En el mundo existen muchos sistemas gestores de bases de datos (SGBD). Uno de los mas conocidos en el mercado es ==Mysql== que actualmente lo mantiene la empresa Oracle, con este gestor vamos a trabajar pero cabe recalcar que como estamos en una distribución de linux entonces usaremos ==Mariadb==.

Mariadb es también un SGBD y es prácticamente igual que Mysql ya que es un Fork de este mismo, una de las diferencias mas grandes es que es open source.

por consiguiente, vamos a verificar que nuestro SGBD este corriendo en nuestro equipo y eso lo hacemos en nuestro emulador de terminal escribiendo el siguiente comando.

```q
systemctl status mariadb
```

Este nos debe arrojar un mensaje por este estilo.

![[Pasted image 20260325222831.png]]

el cual nos indica que el daemon mariadbd esta corriendo y podemos iniciar usando el servicio.

Ahora vamos a iniciar mariadb con el usuario root para crear nuestra primera base de datos, si queremos ingresar con otro usuario debemos de crearlo.

```q
sudo mariadb
```

Nos va a pedir que ingresemos la contraseña, esta es la misma que usamos para iniciar sesión en nuestro computador. Una vez hayamos ingresado la contraseña bien, entonces nos aparecerá lo siguiente en nuestro emulador de terminal.

![[Pasted image 20260325223910.png]]

Estamos listos para poder crear nuestras bases de datos.


## Creación de Bases de Datos


> [!PSEUDOCODIGO]
> CREATE DATABASE nombre_basededatos;
>

- Para la creación de una base de datos usamos la siguiente sentencia
```mysql
CREATE DATABASE supermercado;
```

- Mostrar todas las bases de datos creadas
```mysql
SHOW DATABASES;
```

- Iniciando bases de datos
```mysql
USE supermercado;
```

- Creando tablas
```mysql
CREATE TABLE producto(
	id_producto INT NOT NULL,
	nombre VARCHAR(20) NOT NULL,
	cantidad INT NOT NULL
	precio DECIMAL(10,2) NOT NULL
);
```