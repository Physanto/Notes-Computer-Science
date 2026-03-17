las matrices en álgebra lineal son un conjunto de valores que están organizados por filas y columnas.

## Determinante de una matriz

Es un valor único asociado a una matriz cuadrada $\large n$ x $\large n$ y se calcula con varios métodos, el mas común es el siguiente:

sea la matriz 
$$\large A = 
\begin {pmatrix}
a & b \\
c & d 
\end{pmatrix}$$
el determinante es:
$$\large det(A) = ad - bc$$

## Matriz identidad

Es una matriz cuadrada que esta constituida por 1s en la diagonal y ceros en el resto de las posiciones.

$$\large
I = \begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
$$
## Matriz inversa

La matriz inversa $\large A^{-1}$ de una matriz cuadrada $\large A$ es aquella que, al multiplicarse por la original resulta en la matriz identidad $\large I$.


## Matriz transpuesta

Se denota comúnmente como $\large A^T$ de una matriz A es la operación que consiste en intercambiar filas por columnas.

$$\large A = 
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6
\end{pmatrix}$$
$$\large A^T = 
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6
\end{pmatrix}$$
Si se tiene una matriz $\large A$ con dimensión $\large m$ x $\large n$, su transpuesta $\large A^T$ tendrá una dimensión $\large n$ x $\large m$


## Matriz transpuesta compleja o matriz adjunta

La matriz transpuesta compleja o matriz ajunta se obtiene intercambiando sus filas por columnas y cambiando el signo de la parte imaginaria de cada elemento.

si tenemos 
$$\large U = 
\begin{pmatrix}
1+i & 2 \\
3-i & 4i
\end{pmatrix}$$
Su transpuesta compleja $\large U^*$ es
$$\large U^* = 
\begin{pmatrix}
1-i & 3+i \\
2 & -4i
\end{pmatrix}$$

## Matriz unitaria

Una matriz unitaria es una matriz que al multiplicarse por su adjunta da la matriz identidad, $\large U^†U = I$



## Normalizar matrices

Normalizar matrices significa ajustar (escalar) la matriz para que tenga norma 1, esto se hace multiplicandolas por un numero para que sus columnas o filas tengan longitud 1.

