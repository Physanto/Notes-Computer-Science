
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


### Creando una base de datos.

> [!PSEUDOCODIGO]
> CREATE DATABASE nombre;
> 
> #CREATE: palabra reservada.
> #DATABASE: palabra reservada
> #nombre: es el nombre que se le da a la base de datos que se quiere crear, se recomienda usar la convención ==snake_case o PascalCase==, por ejemplo: Estudiante, detalle_factura.

- Ejemplo:
```mysql
CREATE DATABASE supermercado;
```

### Mostrar las bases de datos creadas.

> [!pseudocodigo]
> SHOW DATABASES;
> 
> #SHOW: palabra reservada.
> #DATABASES: palabra reservada

- Ejemplo:
```mysql
SHOW DATABASES;
```

![[Pasted image 20260326075755.png]]

Como podemos observar nos aparece todas las bases de datos que tenemos creadas.

### Iniciando la base de datos.

> [!pseudocodigo]
> USE nombre;
> 
> #USE: palabra reservada.
> #nombre: representa el nombre de la base de datos que queremos usar.

- Ejemplo:
```mysql
USE supermercado;
```

![[Pasted image 20260326080101.png]]

Este mensaje nos indica que la base de datos ya la estamos usando.

### Creando tablas

> [!pseudocodigo]
> CREATE TABLE nombre (
> nombre_columna1 TIPO_DATO RESTRICCION
> );
> 
> #CREATE: palabra reservada.
> #TABLE: palabra reservada.
> #nombre: nombre de la tabla que se le va a dar.
> #nombre_columna1: el nombre que se le va a dar a la columna
> #TIPO_DATO; Es el tipo de dato que se le va a dar a ese campo. Ej: INT, VARCHAR, DECIMAL.
> #RESTRICCION: Es la restriccion que se le va a dar a ese campo. Ej: NOT NULL

- Ejemplo:

```mysql
CREATE TABLE producto(
	id_producto INT NOT NULL,
	nombre VARCHAR(20) NOT NULL,
	cantidad INT NOT NULL
	precio DECIMAL(10,2) NOT NULL
);
```

Como podemos notar el tipo de dato **VARCHAR(cant)** tiene un argumento este representa la cantidad de caracteres que puede almacenar ese campo.

Al igual que el tipo de dato **DECIMAL(p,s)** tiene argumentos, la p representa la precisión, es decir la cantidad de dígitos en total (incluyendo los decimales)y la s representa la cantidad de dígitos a la derecha del punto decimal.


### Mostrar estructura de la tabla

> [!pseudocodigo]
> DESCRIBE nombre;
> 
> #DESCRIBE: palabra reservada
> #nombre: nombre de la tabla que se quiere mostrar.

- Ejemplo:

```mysql
DESCRIBE producto;
```

![[Pasted image 20260326085957.png]]


### Mostrar todos los datos de una tabla

