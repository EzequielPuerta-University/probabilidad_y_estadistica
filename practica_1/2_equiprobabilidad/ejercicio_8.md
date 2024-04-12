### <a name="8"></a> 8. En un negocio hay 6 productos de cierto tipo, 3 de ellos vencidos y 3 que están dentro del periodo de validez. Si un supervisor, que no sabe cuántos envases válidos o vencidos hay, los revisa, ¿cuál es la probabilidad de que

#### <a name="8.a"></a> 8.a. los tres primeros envases revisados contengan los productos vencidos?

El supervisor va a revisar los 6 productos, ya que no sabe cuantos son los vencidos en total. Nuestro espacio muestral es el siguiente:

```math
Vencidos = \{ v_1, v_2, v_3 \} , \hspace{1em} Válidos = \{ s_1, s_2, s_3 \} \\
\Omega = \{ (x_1, x_2, x_3, x_4, x_5, x_6) | \hspace{0.5em} i,j \in [1..6], x_i \in (Vencidos \cup Válidos), x_i = x_j \iff i = j \}
```

Por lo tanto si tenemos el evento:

```math
A = \{ \text{los 3 primeros envases revisados son los vencidos} \}
```

Tenemos como casos favorables aquellos en los cuales, los 3 productos vencidos son seleccionados primero. Básicamente hay que permutar los vencidos y luego los válidos. Calculemos $P(A)$:

```math
P(A) =
\frac{\text{casos favorables}}{\text{casos totales}} =
\frac{3 \times 2 \times 1 \times 3 \times 2 \times 1}{6 \times 5 \times 4 \times 3 \times 2 \times 1} =
\frac{1}{5 \times 4} =
\frac{1}{20} _\square
```

#### <a name="8.b"></a> 8.b. necesite revisar exactamente $i$ envases para encontrar los tres que contienen los productos vencidos? (hacerlo para $i = 4, 5, 6$).

Llamamos:

```math
A_i = \{ \text{En el $i$-ésimo envase revisado se encuentra el último de los vencidos} \}
```

* $i = 4$

Recién en el cuarto producto se encuentra el tercer producto vencido, por lo que hay un producto válido entre los 3 primeros. Entonces elijo uno de los 3 válidos para ubicar entre los 3 primeros, elijo luego uno de los 3 vencidos para fijarlo en el cuarto lugar, de los 3 primeros lugares elijo 1 para ubicar el único válido, permuto los 2 productos vencidos en los primeros lugares y los 2 productos válidos en los últimos lugares:

```math
P(A_4) =
\frac{\text{casos favorables}}{\text{casos totales}} =
\frac{ \begin{pmatrix} 3 \\ 1 \end{pmatrix} \times \begin{pmatrix} 3 \\ 1 \end{pmatrix} \times \begin{pmatrix} 3 \\ 1 \end{pmatrix} \times 2! \times 2! }{6!} =
\frac{3 \times 4 \times 3! \times 2!}{6!} =
\frac{4! \times 3!}{6!} = \frac{1}{5} _\square
```

* $i = 5$

Recién en el quinto producto se encuentra el tercer producto vencido, por lo que hay dos productos válidos entre los 4 primeros. Entonces elijo dos de los 3 válidos para ubicar entre los 4 primeros, elijo luego uno de los 3 vencidos para fijarlo en el quinto lugar, de los 4 primeros lugares elijo 2 para ubicar los válidos, permuto los 2 productos vencidos en los primeros lugares y los 2 productos válidos en los primeros lugares:

```math
P(A_5) =
\frac{\text{casos favorables}}{\text{casos totales}} =
\frac{ \begin{pmatrix} 3 \\ 2 \end{pmatrix} \times \begin{pmatrix} 3 \\ 1 \end{pmatrix} \times \begin{pmatrix} 4 \\ 2 \end{pmatrix} \times 2! \times 2! }{6!} =
\frac{3 \times 3 \times 6 \times 4}{6!} = \frac{3}{10} _\square
```

* $i = 6$

Recién en el sexto y último producto se encuentra el tercer producto vencido, por lo que hay tres productos válidos entre los 5 primeros. Entonces elijo los 3 válidos para ubicar entre los 5 primeros, elijo luego uno de los 3 vencidos para fijarlo en el sexto lugar, de los 5 primeros lugares elijo 3 para ubicar los válidos, permuto los 2 productos vencidos en los primeros lugares y los 3 productos válidos en los primeros lugares:

```math
P(A_5) =
\frac{\text{casos favorables}}{\text{casos totales}} =
\frac{ \begin{pmatrix} 3 \\ 3 \end{pmatrix} \times \begin{pmatrix} 3 \\ 1 \end{pmatrix} \times \begin{pmatrix} 5 \\ 3 \end{pmatrix} \times 2! \times 3! }{6!} =
\frac{1 \times 3 \times 10 \times 12}{6!} = \frac{1}{2} _\square
```

> [Volver](../README.md)
