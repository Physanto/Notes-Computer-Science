
El método simplex es un algoritmo que se puede representar mediante modelos de programación lineal, este nos permite encontrar la máxima ganancia o el mínimo costo de un problema dado. Matemáticamente es una técnica para optimizar una función objetivo sujeto a restricciones como igualdades o desigualdades [[#Referencias]|[1]]].


### Pasos del método simplex

1. Convertir a la forma estándar
	- todas las restricciones deben ser '<='
	- Agregar variables de holgura (s)

Variable de holgura: es una variable que se agrega a una restricción de desigualdad para transformarla en una restricción de igualdad.

- Ejemplo: $\large 2x+y<=10$  $\large=>$   $\large2x+y+s=10$

 2. Armar la tabla simplex

| Base           | $\large x_{1}$ | $\large x_{2}$ | $\large s_{1}$ | $\large s_{2}$ | Resultado |
| -------------- | -------------- | -------------- | -------------- | -------------- | --------- |
| $\large s_{1}$ | 2              | 1              | 1              | 0              | 10        |
| $\large s_{2}$ | 1              | 3              | 0              | 1              | 15        |
| $\large z$     | -3             | -5             | 0              | 0              | 0         |

 3. Elegir variables entrante 
 
 - Se escoge el coeficiente mas negativo en Z.
 
 3. Elegir variable saliente
 
 - Se divide 

## Referencias

- -[1] Luis A. "Un sistema de apoyo para la enseñanza del método            simplex y su implementacion en computadora"
	   Disponible:scielo.cl/pdf/formuniv/v11n6/0718-5006-formuniv-11-06-29.pdf