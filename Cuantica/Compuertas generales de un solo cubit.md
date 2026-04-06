
Una puerta lógica general de un solo cubit funciona de manera similar, en particular se puede representar como una matriz $\large 2 x 2$ unitaria, $\large U$, [[Matrices en algebra lineal#Matriz unitaria|matrices unitarias]]. Cabe aclarar que las compuertas lógicas $\large X$(NOT) y $\large H$(Hadamard) en su forma matricial son matrices unitarias.


>[!QUESTION]
> - Por que las compuertas de un solo cubit se describen mediante matrices unitarias?
> - Como podemos comprender intuitivamente que significa que una matriz sea unitaria?
> - Supongamos que disponemos de un dispositivo capaz de determinar con exactitud el estado de un cubit. como podria utilizarse dicho dispositivo como parte de un sistema para comunicar informacion clasica infinita, utilizando un solo cubit?

## Comprobando que las compuertas X y H en su forma matricial son unitarias $\large U^{\dagger}U = I $

Primero vamos a ponerla en forma matricial

$$\large H = 
\left(\frac{1}{\sqrt{2}}
\begin{bmatrix}
1 & 1 \\
1 & -1
\end{bmatrix} \right)
$$

ahora calculamos su [[Matrices en algebra lineal#Matriz transpuesta compleja o matriz adjunta|transpuesta compleja]], recordemos que $\large U^\dagger:=(U^T)^*$

$$
\large 
H^{\dagger} = \left( \left(\frac{1}{\sqrt{2}}
\begin{bmatrix}
1 & 1 \\
1 & -1
\end{bmatrix}
\right) ^T
\right) ^*
$$

resolviendo tenemos

$$ 
\large H^{\dagger} = \left(\frac{1}{\sqrt2}
\begin{bmatrix}
1 & 1 \\
1 & -1
\end{bmatrix}
\right)
$$

como ya resolvimos la transpuesta compleja ahora vamos a multiplicarla por la matriz original.

$$
\large H^{\dagger} \cdot H = \left(\frac{1}{\sqrt{2}}
\begin{bmatrix}
1 & 1 \\
1 & -1
\end{bmatrix}
\right) 
\cdot 
\left(
\frac{1}{\sqrt{2}}
\begin{bmatrix}
1 & 1 \\
1 & -1
\end{bmatrix}
\right)
$$

$$ 
\large = \begin {bmatrix}
1 & 1 \\
1 & -1
\end{bmatrix}
\cdot
\begin {bmatrix}
1 & 1 \\
1 & -1
\end{bmatrix}
= \begin {bmatrix}
2 & 0 \\
0 & 2
\end{bmatrix} 
$$

$$
\large = \frac{1}{\sqrt2} \cdot \frac{1}{\sqrt2} = \frac{1}{(\sqrt2)^2} = \frac {1}{2} 
$$

Uniendo las partes nos queda

$$ 
\large \frac{1}{2} \cdot \begin {bmatrix} 2 & 0 \\ 0 & 2 \end {bmatrix}
$$
por ultimo resolvemos esta operación que consta de un escalar por una matriz y nos da
$$
\large \begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix} = I
$$

entonces podemos decir que la puerta lógica cuántica $\large H$ en su representación matricial es una matriz unitaria $\large H^\dagger \cdot H = I$


## Que significa que una matriz sea unitaria?

Significa que al multiplicarse por un vector de n-dimensiones conserva la [[Matrices en algebra lineal#Longitud de un vector|longitud]] de dicho vector.
