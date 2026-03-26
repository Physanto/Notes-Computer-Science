
## DDL (Data Definition Language)

Es un conjunto de comandos en [[SQL|SQL]] que se utilizan para crear, modificar y eliminar objetos de una base de datos. En otras palabras el DDL define la estructura de la base de datos.

> [!QUESTION]
> 1. ¿Que es la estructura de una base de datos?
> 2. ¿Que es un objeto en bases de datos?
> <br>
> >[!ANSWER]
> >
> > <br>
> >
> > 1. Se refiere a como esta organizada la base de datos internamente, no a los datos en si. En términos mas simples, es el **plano o esqueleto** de la base de datos [[#Referencias|[1]]].
> > ^a-estructura
> >
> > <br>
> > 
> > 2. Son las piezas que componen a una base de datos y cada una de estas tienen una función especifica.


### Comandos Básicos

- ==CREATE==: Se utiliza para crear nuevos objetos, como bases de datos, tablas, vistas, indices, etc.

- ==ALTER==: Permite modificar la estructura de los objetos, como añadir o eliminar columnas, cambiar el tipo de dato, etc.

- ==DROP==: Se emplea para eliminar objetos, como eliminar la base de datos existente, tabla, etc.

- ==TRUNCATE==: Este comando se encarga de eliminar todos los datos de la tabla pero no su estructura.

> [!NOTE]
> Estos comandos solo permiten la manipulación de la [[#^a-estructura|estructura de la base de datos]].

### Importancia de DDL

El DDL es una herramienta esencial, ya que permite definir y gestionar la estructura de una base de datos de manera eficiente. Utilizamos sentencias DDL para establecer el marco o la [[#^a-estructura|estructura de una base de datos]].


### Objetos de las Bases de Datos





## Referencias

- -[1] DataSunrise, "Comprendiendo DDL: Lenguaje de definición              de datos en bases de datos,"
	    Disponible: https://www.datasunrise.com/es/centro-de-conocimiento/ddl-lenguaje-de-definicion-de-datos/
		
- -[2]