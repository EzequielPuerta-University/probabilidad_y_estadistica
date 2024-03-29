### <a name="3"></a> 3. En el tablero de la figura,

![Figura1.1.3](../img/1_1_3.png)

### ¿cuántas formas hay de llegar desde *A* hasta *B* realizando movimientos hacia abajo y hacia la derecha siguiendo las líneas? ¿Cuántos de esos caminos pasan por $X$? Generalizar para un tablero de tamaño $n \times m$.

Observo que como no puedo volver sobre mis pasos, solo puedo avanzar hacia $B$ en alguna de las direcciones mencionadas, cualquiera sea el camino que tome estará compuesto por la misma cantidad de pasos hacia la derecha y hacia abajo. Llamemos:

```math
\begin{align}
    d_B &= \#D_B = \#\{d_1, d_2, ... , d_8 \} = 8 = \text{la cantidad de pasos horizontales que separan $A$ y $B$} \\
    a_B &= \#A_B = \#\{a_1, a_2, ... , a_5 \} = 5 = \text{la cantidad de pasos verticales que separan $A$ y $B$}
\end{align}
```

Podemos definir entonces nuestros caminos válidos como:

```math
C_B = \{(c_1, c_2, c_3, ... , c_{13}) \hspace{0.5em} | \hspace{0.5em} c_i \in A_B \cup D_B , \hspace{0.5em} 1 \leq j,k \leq 13 , \hspace{0.5em} c_j = c_k \iff j = k \}
```

Por lo tanto, tenemos 13 movimientos disponibles y necesarios para llegar a $B$ desde $A$. Todos los caminos dentro de $C_B$ contienen los mismos movimientos en distinto orden. Si consideramos las permutaciones, nos acercaremos a la respuesta:

```math
13!
```

Son muchos caminos. Estamos contando repetidos. Veamos el siguiente ejemplo:

```math
\begin{align}
    c_{B_1} &= (a_1, a_2, a_3, a_4, a_5, d_1, d_2, d_3, d_4, d_5, d_6, d_7, d_8) \\
    c_{B_2} &= (a_5, a_4, a_3, a_2, a_1, d_1, d_2, d_3, d_4, d_5, d_6, d_7, d_8)
\end{align}
```

Son dos caminos válidos, formalmente distintos, pero que en la práctica son idénticos. Estamos distinguiendo los movimientos en el mismo sentido con un subindice por comodidad para la definición del conjunto, pero en realidad los movimientos en el mismo sentido no son distinguibles, por lo tanto repetimos caminos.

Entonces debemos quitar los repetidos dividiendo por las permutaciones de sendos sentidos:

```math
\frac{13!}{5! \times 8!} {}_\square
```

Ahora bien, ¿cuantos de estos caminos pasarán por $X$? Para llegar a $X$ tendremos que movernos 3 posiciones hacia la derecha y 3 hacia abajo, nuevamente sin importar el orden. Entonces un camino $c \in C_B$ que pase por $X$, debería tener en sus primeros 6 movimientos alguna permutación de 3 pasos hacia la derecha y 3 pasos hacia abajo. Formalizo los caminos válidos entre $A$ y $X$ de la siguiente manera:

```math
C_X = \{(c_1, c_2, c_3, ... , c_6) \hspace{0.5em} | \hspace{0.5em} c_i \in \{a_1, a_2, a_3\} \cup \{d_1, d_2, d_3\} , \hspace{0.5em} 1 \leq j,k \leq 6 , \hspace{0.5em} c_j = c_k \iff j = k \}
```

Por lo que para que $c \in C_B$ pase por $X$, debe valer también que $c \in C_{XB}$, con:

```math
C_{XB} = \{(c_1, c_2, c_3, ... , c_{13}) = c \hspace{0.5em} | \hspace{0.5em} c \in C_B, \hspace{0.5em} (c_1, c_2, c_3, c_4, c_5, c_6) \in C_X \}
```

Pasando en limpio, primero debemos permutar el camino hasta $X$ para obtener la cantidad de todos los caminos posibles (con repetidos):

```math
(3+3)! = 6!
```

Y dividimos por las permutaciones de ambos sentidos, para eliminar las repeticiones:

```math
\frac{6!}{3! \times 3!} = \frac{6 \times 5 \times 4}{3 \times 2 \times 1} = \frac{5 \times 4}{1} = 20 _\square
```

> [Volver](../README.md)
