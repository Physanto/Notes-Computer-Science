
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


### Creando una base de datos (CREATE).

> [!Estructura]
> CREATE DATABASE nombre;
> 
> #CREATE: palabra reservada (==Crear==).
> #DATABASE: palabra reservada (==Base de Datos==).
> #nombre: es el nombre que se le da a la base de datos que se quiere crear, se recomienda usar la convención ==snake_case o PascalCase==, por ejemplo: Estudiante, detalle_factura.

> [!Tip]
> Se lee: crear una base de datos llamada (nombre de la base de datos).

> [!Warning]
> Cada sentencia SQL se debe finalizar con punto y coma (;).

- Ejemplo en SQL:
```mysql
CREATE DATABASE supermercado;
```

### Mostrar las bases de datos creadas (SHOW).

> [!Estructura]
> SHOW DATABASES;
> 
> #SHOW: palabra reservada (==mostrar==).
> #DATABASES: palabra reservada (==bases de datos==)

> [!Tip]
> Se lee: Mostrar todas las bases de datos.

- Ejemplo en SQL:
```mysql
SHOW DATABASES;
```

![[Pasted image 20260408212904.png]]

Como podemos observar nos aparece todas las bases de datos que tenemos creadas.

### Iniciando la base de datos (USE).

> [!Estructura]
> USE nombre;
> 
> #USE: palabra reservada (==Usar==).
> #nombre: representa el nombre de la base de datos que queremos usar.

> [!Tip]
> Se lee: Usa la base de datos (nombre de la base de datos).

- Ejemplo:
```mysql
USE supermercado;
```

![[Pasted image 20260326080101.png]]

Este mensaje nos indica que la base de datos ya la estamos usando.

### Creando tablas (CREATE)

> [!Estructura]
> CREATE TABLE nombre (
> nombre_columna1 TIPO_DATO RESTRICCION
> );
> 
> #CREATE: palabra reservada (==Crear==).
> #TABLE: palabra reservada (==Tabla==).
> #nombre: nombre de la tabla que se le va a dar.
> #nombre_columna1: el nombre que se le va a dar a la columna
> #TIPO_DATO; Es el tipo de dato que se le va a dar a ese campo. Ej: INT, VARCHAR, DECIMAL.
> #RESTRICCION: Es la restriccion que se le va a dar a ese campo. Ej: NOT NULL.

> [!Tip]
> Se lee: Crear una tabla llamada ... la cual va tener una columna con nombre ... de tipo ... con restriccion ...

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

### Mostrar estructura de la tabla (DESCRIBE).

> [!Estructura]
> DESCRIBE nombre;
> 
> #DESCRIBE: palabra reservada (==Describir==).
> #nombre: nombre de la tabla que se quiere mostrar.

> [!Tip]
> Se lee: Describe la tabla (nombre de la tabla).

- Ejemplo:
```mysql
DESCRIBE producto;
```

![[Pasted image 20260326085957.png]]

### Insertar datos en una tabla (INSERT)

> [!Estructura]
> INSERT INTO nombre_tabla (column1, column2, ...)
> VALUES (valor1, valor2, ...);
> 
> #INSERT: palabra reservada que indica (==Insertar==).
> #INTO: palabra reservada que indica (==Dentro==).
> #nombre_tabla: es el nombre de la tabla donde queremos ingresar los datos.
> #colum1, #colum2 ...: nombre de las columnas de la tabla que ya fueron definidas anteriormente.
> #VALUES: palabra reservada que indica (==Valores==).
> #valor1, #valor2...: aquí ya se ingresa el valor que se le quiere dar a la columna.

> [!Warning]
> Cuando se vaya a poner el valor en la columna se debe tener muy en cuenta el tipo de dato que previamente se ha definido para esa columna, por ejemplo: 
> - columna1 es de tipo INT entonces se pone el numero tal cual.
> - columna2 es de tipo VARCHAR entonces se debe poner los caracteres entre comillas dobles (==" "==).

> [!Tip]
> - Se lee: insertar dentro de la tabla (nombre de la tabla) en todas sus columnas los valores (el valor a cada columna).
> - se pueden ingresar cualquier cantidad de valores, solo se debe tener en cuenta que cada grupo de valores se separa con una coma.

- Ejemplo:
```mysql
INSERT INTO producto (id_producto, nombre, cantidad, precio)
VALUES 
(1, "Memoria RAM", 10, 250000),
(2, "CPU", 15, 500000),
(3, "Disco Duro", 8, 300000);
```

### Mostrar los datos de una tabla (SELECT)

Para esta parte tenemos dos formas de poder mostrar los datos de una tabla.

#### Mostrando datos de campos específicos de una tabla.

> [!Estructura]
> SELECT nombre_columna1, nombre_columna2, ... FROM nombre_tabla
> #SELECT: palabra reservada que indica (==Seleccionar==).
> #nombre_columna1: representa el nombre de la columna de la tabla.
> #FROM: palabra reservada que indica (==de==).
> #nombre_tabla: es el nombre de la tabla de donde se quiere mostrar los datos.

> [!Tip]
> Se lee: selecciona los elementos de la columnas descritas la tabla producto.

- Ejemplo:
```mysql
SELECT nombre, precio FROM producto;
```

![[Pasted image 20260408222221.png]]

#### Mostrando todos los datos de una tabla

> [!Estructura]
> SELECT * FROM nombre_tabla;
> 
> #SELECT: palabra reservada que indica (==seleccionar==).
> #SIGNO*: representa todos los datos.
> #FROM: palabra reservada que indica (==de==).
> #nombre_tabla: es el nombre de la tabla de donde se quiere mostrar los datos.

> [!Tip]
> Se lee: selecciona todos los elementos de la tabla producto.

- Ejemplo:
```mysql
SELECT * FROM producto;
```

![[Pasted image 20260408222320.png]]