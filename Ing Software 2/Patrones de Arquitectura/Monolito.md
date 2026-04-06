
Un patrón de arquitectura en software es básicamente una receta, idea o sugerencia de como se debe estructurar un proyecto de software.



## Patrones de Bajo Nivel


### Singleton

El patrón singleton es un patrón de nivel bajo en términos de abstracción.

### Caracteristicas del patron

- Control de instancia

- enfoque de implementacion concreta

- Singleton

el patron singleton esta aplicado en la clase conexion


### Patron Metodo Plantilla

Es un patron de nivel bajo en terminos de abstraccion, se centra en la implementacion de una clase en concreto

este patron esta aplicado en la clase abstracta de usuario en la capa de logica de negocio

el metodo plantilla se usa siempre



## Patrones de nivel medio

Estos patrones se centran en la interaccion de los objetos.


### Adapter

el adaptador se usa cuando se conecta en una base de datos en la nube con una clase concreta por ejemplo

en una base de datos en la nube la conexion espera una clave, valor pero mi clase me retorna un objeto.


## DAO(Data Access Object)

Es un patrón de nivel medio en términos de abstracción, aunque se centra en la interacción con bases de datos y la persistencia de datos.

nos ayuda abstraer la lógica de negocio con la lógica de acceso a datos.



## Patrones de alto nivel

El patrón de arquitectura en capas


- Nos permite estructurar el sistema de manera global
- separar responsabilidades

Capa de presentacion
Capa de acceso datos = dao, plantilla
Capa de logica de negocio = ad