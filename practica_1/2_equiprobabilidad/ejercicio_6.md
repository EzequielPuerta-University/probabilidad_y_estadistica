### <a name="6"></a> 6. Un grupo de 60 alumnos será subdividido al azar en dos divisiones de 30 alumnos cada una. Cinco de esos alumnos son muy amigos.: Alicia, Beto, Carmen, Diego y Eva:

#### <a name="6.a"></a> 6.a. ¿Cuál es la probabilidad de que todos queden en la misma división?

Para que todos queden juntos, deberíamos ubicarlos en la misma división y completar los 25 restantes con otros alumnos disponibles de los otros 55:

```math
A = \{ \text{Los 5 amigos quedan en la misma división} \}
```

```math
\begin{align}
P(A) &= \frac{\text{casos\_positivos}_A}{\text{casos\_totales}} =
\frac{\begin{pmatrix} 55 \\ 25 \end{pmatrix}}{\begin{pmatrix} 60 \\ 30 \end{pmatrix}} \\
P(A) &= \frac{\frac{55!}{25! \times 30!}}{\frac{60!}{30! \times 30!}} \\
P(A) &= \frac{\bcancel{55!}}{\cancel{25!} \times \xcancel{30!}} \times \frac{\xcancel{30!} \times \cancel{30!}}{\bcancel{60!}} \\
P(A) &= \frac{30 \times 29 \times 28 \times 27 \times 26}{60 \times 59 \times 58 \times 57 \times 56} \\
P(A) &= \frac{1 \times 1 \times 1 \times 9 \times 13}{2 \times 59 \times 2 \times 19 \times 1} \\
P(A) &= \frac{117}{4484} \\
P(A) &= 0.026092774 _\square
\end{align}
```

#### <a name="6.b"></a> 6.b. ¿Cuál es la probabilidad de que sólo quede separado Diego?

Como Diego queda separado, solo tenemos a 4 de los amigos en la misma división, por lo que tendremos que completarla con 26 alumnos mas, elegidos entre los 55 restantes (todos los demás que no son Diego, para no ingresarlo con el grupo de 4 amigos):

```math
B = \{ \text{Solo Diego queda separado del grupo} \}
```

```math
\begin{align}
P(B) &= \frac{\text{casos\_positivos}_A}{\text{casos\_totales}} =
\frac{\begin{pmatrix} 55 \\ 26 \end{pmatrix}}{\begin{pmatrix} 60 \\ 30 \end{pmatrix}} \\
P(B) &= \frac{\frac{55!}{26! \times 29!}}{\frac{60!}{30! \times 30!}} \\
P(A) &= \frac{\bcancel{55!}}{\cancel{26!} \times \xcancel{29!}} \times \frac{\xcancel{30!} \times \cancel{30!}}{\bcancel{60!}} \\
P(B) &= \frac{30 \times 30 \times 29 \times 28 \times 27}{60 \times 59 \times 58 \times 57 \times 56} \\
P(B) &= \frac{1 \times 15 \times 1 \times 1 \times 27}{2 \times 59 \times 2 \times 57 \times 1} \\
P(B) &= \frac{405}{13452} \\
P(B) &= 0.030107047 _\square
\end{align}
```

> [Volver](../README.md)
