
Una puerta lógica general de un solo cubit funciona de manera similar, en particular se puede representar como una matriz $\large 2 x 2$ unitaria, $\large U$, [[Matrices en algebra lineal#Matriz unitaria|matrices unitarias]]. Cabe aclarar que las compuertas lógicas $\large X$(NOT) y $\large H$(Hadamard) en su forma matricial son matrices unitarias.


>[!NOTE]
> - Por que las compuertas de un solo cubit se describen mediante matrices unitarias?
> - Como podemos comprender intuitivamente que significa que una matriz sea unitaria?

## Comprobando que las compuertas X y H en su forma matricial son unitarias $\large U^{\dagger}U = I$

Primero vamos a ponerla en forma matricial

$$\large H = \left(
\frac{1}{\sqrt{2}}
\begin{bmatrix}
1 & 1 \\
1 & -1
\end{bmatrix}
\right)
$$

ahora calculamos su [[Matrices en algebra lineal#Matriz transpuesta compleja o matriz adjunta|trasnpuesta compleja]]

$$\large H^{\dagger} = \left(
\frac{1}{\sqrt{2}}
\begin{bmatrix}
1 & 1 \\
1 & -1
\end{bmatrix}
\right)
$$

podemos observar que al calcularla no cambia