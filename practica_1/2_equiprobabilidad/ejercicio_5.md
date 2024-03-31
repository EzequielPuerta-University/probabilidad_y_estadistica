### <a name="5"></a> 5. Una firma proveedora de software ha ofrecido sus servicios a 3 empresas. Se definen los eventos $A_i$ = {la empresa $i$ realiza una compra a esta firma} , para $i = 1, 2, 3$. Se sabe que:

```math
\begin{array}{ccc}
P(A_1)=0.22 & P(A_2)=0.25 & P(A_3)=0.28 \\
P(A_1 \cap A_2)=0.11 & P(A_1 \cap A_3)=0.05 & P(A_2 \cap A_3)=0.07 \\
P(A_1 \cap A_2 \cap A_3)=0.01
\end{array}
```

 Expresar en palabras los siguientes eventos y calcular sus probabilidades:

```math
\begin{array}{ccc}
A_1 \cup A_2 & A^C_1 \cap A^C_2 & A_1 \cup A_2 \cup A_3 \\
A^C_1 \cap A^C_2 \cap A^C_3 & A^C_1 \cap A^C_2 \cap A_3 & (A^C_1 \cap A^C_2) \cup A_3
\end{array}
```

#### * $A_1 \cup A_2$

Es el conjunto de eventos en los que las empresas 1 y 2 realizan compras a la firma, simultáneamente o no.

```math
\begin{align}
P(A_1 \cup A_2) &= P(A_1) + P(A_2) - P(A_1 \cap A_2) = \\
P(A_1 \cup A_2) &= 0.22 + 0.25 - 0.11 \\
P(A_1 \cup A_2) &= 0.36 _\square
\end{align}
```

#### * $A_1^{C} \cap A_2^{C}$

Es el conjunto de eventos en los que ni la empresa 1 ni la 2 realizan compras a la firma.

```math
\begin{align}
P(A_1^{C} \cap A_2^{C}) &= 1 - P(A_1 \cup A_2) \\
P(A_1^{C} \cap A_2^{C}) &= 1 - 0.36 \\
P(A_1^{C} \cap A_2^{C}) &= 0.64 _\square
\end{align}
```

#### * $A_1 \cup A_2 \cup A_3$

Es el conjunto de eventos en los que alguna de las 3 empresas realizan compras a la firma (pueden ser varias simultáneamente).

```math
\begin{align}
P(A_1 \cup A_2 \cup A_3) &= \\
P(A_1) + P(A_2) + P(A_3) - P(A_1 \cap A_2) - P(A_1 \cap A_3) - P(A_2 \cap A_3) + P(A_1 \cap A_2 \cap A_3) &= \\
0.22 + 0.25 + 0.28 - 0.11 - 0.05 - 0.07 + 0.01 &= \\
0.53 _\square
\end{align}
```

#### * $A^C_1 \cap A^C_2 \cap A^C_3$

Es el conjunto de eventos en los que ninguna de las 3 empresas realizan compras a la firma.

```math
\begin{align}
P(A^C_1 \cap A^C_2 \cap A^C_3) &= 1 - P(A_1 \cup A_2 \cup A_3) \\
P(A^C_1 \cap A^C_2 \cap A^C_3) &= 1 - 0.53 \\
P(A^C_1 \cap A^C_2 \cap A^C_3) &= 0.47 _\square
\end{align}
```

#### * $A^C_1 \cap A^C_2 \cap A_3$

Es el conjunto de eventos en los que solo la empresa 3 realiza compras a la firma.

```math
\begin{align}
P(A^C_1 \cap A^C_2 \cap A_3) &= P(A_3) - P(A_1 \cap A_3) - P(A_2 \cap A_3) + P(A_1 \cap A_2 \cap A_3) \\
P(A^C_1 \cap A^C_2 \cap A_3) &= 0.28 - 0.05 - 0.07 + 0.01 \\
P(A^C_1 \cap A^C_2 \cap A_3) &= 0.17 _\square
\end{align}
```

#### * $(A^C_1 \cap A^C_2) \cup A_3$

Es el conjunto de eventos en el que ni la empresa 1 ni la 2 realizan compras, sumado a aquellos en los que la empresa 3 sí realiza compras (pudiendo darse el caso que alguna(s) de las empresas restantes también compre(n)).

```math
\begin{align}
P((A^C_1 \cap A^C_2) \cup A_3) &= P(A^C_1 \cap A^C_2) + P(A_1 \cap A_3) + P(A_2 \cap A_3) - P(A_1 \cap A_2 \cap A_3) \\
P((A^C_1 \cap A^C_2) \cup A_3) &= P(A^C_1 \cap A^C_2) + 0.05 + 0.07 - 0.01 \\
P((A^C_1 \cap A^C_2) \cup A_3) &= P(A^C_1 \cap A^C_2) + 0.11 \\
P((A^C_1 \cap A^C_2) \cup A_3) &= (1 - P(A_1 \cup A_2)) + 0.11 \\
P((A^C_1 \cap A^C_2) \cup A_3) &= (1 - (P(A_1) + P(A_2) - P(A_1 \cap A_2))) + 0.11 \\
P((A^C_1 \cap A^C_2) \cup A_3) &= (1 - (0.22 + 0.25 - 0.11)) + 0.11 \\
P((A^C_1 \cap A^C_2) \cup A_3) &= (1 - 0.36) + 0.11 \\
P((A^C_1 \cap A^C_2) \cup A_3) &= 0.75 _\square
\end{align}
```

> [Volver](../README.md)
