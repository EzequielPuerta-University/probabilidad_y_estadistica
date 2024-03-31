### <a name="6.a"></a> 6.a. ¿Cuántos anagramas de **BIBLIOTECARIA** pueden formarse?

Los anagramas son palabras (pueden no tener sentido en nuestro lenguaje coloquial), que se forman usando las mismas letras (y la misma cantidad de ocurrencias) de una palabra original, en este caso ***BIBLIOTECARIA***. En definitiva, es una permutación (considerando que pueden haber letras repetidas) de dicha palabra. Será útil considerar las repeticiones de cada uno de los caracteres:

```math
BIBLIOTECARIA = \begin{cases}
   \#B &= 2 \\
   \#I &= 3 \\
   \#L &= 1 \\
   \#O &= 1 \\
   \#T &= 1 \\
   \#E &= 1 \\
   \#C &= 1 \\
   \#A &= 2 \\
   \#R &= 1
\end{cases}
```

Primero contemos la cantidad total de permutaciones sin importar las letras repetidas. Son 13 letras, por lo tanto:

```math
13!
```

Ahora bien, la letra ***B***, ***I*** y ***A*** se repiten, por lo que hay que eliminar los casos que tengan permutaciones entre caracteres de letra equivalente:

```math
\frac{13!}{3! \times 2! \times 2!} _\square
```

### <a name="6.b"></a> 6.b. ¿Y con la condición de que la T esté a la derecha de la C?

Si la ***T*** tiene que estar a la derecha de la ***C***, podemos subdividir el problema en varios subproblemas disjuntos, por ejemplo considerando la ubicación de la ***C*** y la cantidad de letras que hay hasta la ***T***:

En un primer caso consideremos que la ***C*** se ubica como primer letra, por lo que la ***T*** tiene 12 ubicaciones posibles, o lo que es lo mismo, hay que buscar la cantidad de permutaciones (considerando que aún hay letras repetidas), descartando la letra ***C***:

```math
\frac{12!}{3! \times 2! \times 2!}
```

Que reescrito para conveniencia futura es equivalente a:

```math
12 \times \frac{11!}{3! \times 2! \times 2!}
```

Ahora queremos ver la cantidad de casos siendo que la ***C*** se ubica en la segunda posición. Entonces nos quedan 11 lugares para la ***T***. Y luego tendremos 10 lugares libres a la derecha de la ***C*** más la primera ubicación que sigue libre, para ubicar las 12 letras restantes (recordando que hay repetidos):

```math
11 \times \frac{11!}{3! \times 2! \times 2!}
```

Luego, fijamos la letra ***C*** en la tercer posición. Repetimos la lógica y vemos que tenemos 10 lugares para la ***T***, y 11 en total para las demás letras:

```math
10 \times \frac{11!}{3! \times 2! \times 2!}
```

Se empieza a vislumbrar el patrón:

```math
\begin{align}
\sum_{i=1}^{12} \left( (13-i) \times \frac{11!}{3! \times 2! \times 2!} \right) &= \\
\left( \sum_{i=1}^{12} 13-i \right) \times \frac{11!}{3! \times 2! \times 2!} &= \\
\left( \sum_{i=1}^{12} i \right) \times \frac{11!}{3! \times 2! \times 2!} &= \\
\frac{12 \times 13}{2} \times \frac{11!}{3! \times 2! \times 2!} &= \\
\frac{13!}{2 \times 4!} _\square
\end{align}
```

Vale la pena señalar que si usamos combinatoria, podríamos llegar al mismo resultado. Es decir, si tenemos 13 caracteres y tenemos que seleccionar 2 ubicaciones para la ***C*** y la ***T***, es tan fácil como usar el *número combinatorio* para seleccionar las ubicaciones de ambas letras y luego multiplicar dichos casos por los generados por los 11 caracteres restantes, descontando sus repeticiones por letras equivalentes:

```math
\begin{align}
\begin{pmatrix} 13 \\ 2 \end{pmatrix} \times \frac{11!}{3! \times 2! \times 2!} &= \\
\frac{13!}{2! \times 11!} \times \frac{11!}{3! \times 2! \times 2!} &= \\
\frac{13!}{2 \times 4!} _\square
\end{align}
```

Usaremos ésta técnica para los ejercicios siguientes.

### <a name="6.c"></a> 6.c. ¿Y con la condición de que la T esté a la derecha de la C y la C a la derecha de la R?

Ahora tenemos una condición mas compleja, que involucra 3 letras distintas (ninguna de ellas tiene repeticiones en la palabra original). Usando el segundo método del ejercicio anterior, obtenemos:

```math
\begin{align}
\begin{pmatrix} 13 \\ 3 \end{pmatrix} \times \frac{10!}{3! \times 2! \times 2!} &= \\
\frac{13!}{3! \times 10!} \times \frac{10!}{3! \times 2! \times 2!} &= \\
\frac{13!}{6 \times 4!} _\square
\end{align}
```

### <a name="6.d"></a> 6.d. ¿Y con la condición de que las dos A no estén juntas?

Tal vez es mas fácil y directo buscar el complemento. Los casos de anagramas donde las ***A*** no están juntas, son equivalentes al total menos los casos de anagramas donde las ***A*** efectivamente están juntas. Esto puede ser mucho mas fácil de resolver. Para empezar, la cantidad de anagramas totales ya la tenemos (del primer inciso). Luego, considerar los casos con ***A*** juntas, es equivalente a considerar que tenemos en realidad 12 caracteres, ya que uno de ellos siempre irá agrupado como un par ***AA***, por lo que requerimos una posición menos.

Por lo tanto, debemos encontrar la manera de elegir una de esas 12 posiciones para nuestro par ***AA***, para luego permutar las letras restantes en las 11 posiciones que nos sobren, considerando siempre que habrá otras letras repetidas mas allá de las ***AA*** ya utilizadas:

```math
\begin{pmatrix} 12 \\ 1 \end{pmatrix} \times \frac{11!}{3! \times 2!} = \frac{12!}{1! \times 11!} \times \frac{11!}{3! \times 2!} = \frac{12!}{2 \times 3!}
```

Una vez obtenido el anterior resultado, buscamos el complemento mencionado:

```math
\begin{align}
\frac{13!}{3! \times 2! \times 2!} - \frac{12!}{2 \times 3!} &= \\
\frac{13!}{4 \times 3!} - \frac{12!}{2 \times 3!} &= \\
\left( \frac{13}{2} \times \frac{12!}{2 \times 3!} \right) - \frac{12!}{2 \times 3!}_\square &= \\
\left(\frac{13}{2} - 1 \right) \times \frac{12!}{2 \times 3!} &= \\
\frac{11}{2} \times \frac{12!}{2 \times 3!} &= \\
11 \times \frac{12!}{4!} _\square
\end{align}
```

### <a name="6.e"></a> 6.e. ¿Y con la condición de que todas las vocales estén juntas?

Ahora nos piden agrupar las vocales (y consecuentemente, las consonantes), por lo que será útil ver las letras que disponemos, pero ésta vez agrupadas como corresponde:

```math
\begin{align}
Vocales(BIBLIOTECARIA) = \begin{cases}
   \#I &= 3 \\
   \#O &= 1 \\
   \#E &= 1 \\
   \#A &= 2
\end{cases}
\\
Consonantes(BIBLIOTECARIA) = \begin{cases}
   \#B &= 2 \\
   \#L &= 1 \\
   \#T &= 1 \\
   \#C &= 1 \\
   \#R &= 1
\end{cases}
\end{align}
```

Hecho esto, podemos permutar ambos subconjuntos de letras por separado, y luego considerar el caso cuando las vocales aparecen antes que las consonantes y viceversa:

```math
2 \times \left( \frac{7}{3! \times 2!} \right) \times \left( \frac{6!}{2!} \right)
```

> [Volver](../README.md)
