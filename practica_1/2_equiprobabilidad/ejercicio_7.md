### <a name="7"></a> 7. De un grupo de 6 mujeres y 4 hombres se deben elegir 3 personas para que los representen en tres congresos a desarrollarse en mayo, junio y septiembre.

#### <a name="7.a"></a> 7.a. Suponiendo que una persona puede ir a más de un congreso, calcular la probabilidad de que:

##### <a name="7.a.1"></a> 7.a.1. $A=\{\text{a los dos primeros congresos vayan mujeres.}\}$

Nos piden que nos aseguremos que en los dos primeros congresos vayan mujeres, pero no hay condición alguna sobre quien va al tercer congreso, por lo tanto puede ir una mujer o un hombre. Por otro lado, una misma persona podría ir a los 3 congresos. Finalmente, tenemos 10 personas en total.

```math
\begin{align}
P(A) &= \frac{\text{casos\_positivos}_A}{\text{casos\_totales}} \\
P(A) &= \frac{6 \times 6 \times \cancel{10}}{10 \times 10 \times \cancel{10}} \\
P(A) &= \frac{3 \times 3}{5 \times 5} \\
P(A) &= \frac{9}{25} _\square
\end{align}
```

##### <a name="7.a.2"></a> 7.a.2. $B=\{\text{a los dos primeros congresos vayan mujeres y al tercero un hombre.}\}$

Ahora sí nos condicionan el tercer congreso, debe ir un hombre:

```math
\begin{align}
P(B) &= \frac{\text{casos\_positivos}_B}{\text{casos\_totales}} \\
P(B) &= \frac{\cancel{6} \times \cancel{6} \times \cancel{4}}{\cancel{10} \times \cancel{10} \times \cancel{10}} \\
P(B) &= \frac{3 \times 3 \times 2}{5 \times 5 \times 5} \\
P(B) &= \frac{18}{125} _\square
\end{align}
```

##### <a name="7.a.3"></a> 7.a.3. $C=\{\text{haya por lo menos una mujer entre las 3 personas elegidas.}\}$

Ahora nos piden que por lo menos haya una mujer entre los congresistas. Puede ocurrir que haya una única mujer en un único congreso, que haya una única mujer y que vaya a múltiples congresos, o puede que hayan varias mujeres en varios congresos. Son varias situaciones, quizás lo mas fácil es calcular el complemento, que no haya ninguna mujer entre los elegidos.

```math
\begin{align}
P(C^C) &= \frac{\text{casos\_positivos}_{C^C}}{\text{casos\_totales}} \\
P(C^C) &= \frac{\cancel{4} \times \cancel{4} \times \cancel{4}}{\cancel{10} \times \cancel{10} \times \cancel{10}} \\
P(C^C) &= \frac{2 \times 2 \times 2}{5 \times 5 \times 5} \\
P(C^C) &= \frac{8}{125} \\

&=> \\

P(C) &= 1 - P(C^C) = 1 - \frac{8}{125} = \frac{117}{125} _\square
\end{align}
```

#### <a name="7.b"></a> 7.b. Si a cada congreso debe ir una persona diferente, calcular las mismas probabilidades que en (7.a) y además la probabilidad de que haya exactamente una mujer entre las 3 personas elegidas.

##### <a name="7.b.1"></a> 7.b.1. $A=\{\text{a los dos primeros congresos vayan mujeres.}\}$

```math
\begin{align}
P(A) &= \frac{\text{casos\_positivos}_A}{\text{casos\_totales}} \\
P(A) &= \frac{\bcancel{6} \times \cancel{5} \times \xcancel{8}}{\cancel{10} \times \bcancel{9} \times \xcancel{8}} \\
P(A) &= \frac{\cancel{2}}{\cancel{2} \times 3} \\
P(A) &= \frac{1}{3} _\square
\end{align}
```

##### <a name="7.b.2"></a> 7.b.2. $B=\{\text{a los dos primeros congresos vayan mujeres y al tercero un hombre.}\}$

```math
\begin{align}
P(B) &= \frac{\text{casos\_positivos}_B}{\text{casos\_totales}} \\
P(B) &= \frac{\bcancel{6} \times \cancel{5} \times \xcancel{4}}{\cancel{10} \times \bcancel{9} \times \xcancel{8}} \\
P(B) &= \frac{\cancel{2}}{\cancel{2} \times 3 \times 2} \\
P(B) &= \frac{1}{6} _\square
\end{align}
```

##### <a name="7.b.3"></a> 7.b.3. $C=\{\text{haya por lo menos una mujer entre las 3 personas elegidas.}\}$

```math
\begin{align}
P(C^C) &= \frac{\text{casos\_positivos}_{C^C}}{\text{casos\_totales}} \\
P(C^C) &= \frac{\cancel{4} \times \bcancel{3} \times \cancel{2}}{10 \times \bcancel{9} \times \cancel{8}} \\
P(C^C) &= \frac{1}{10 \times 3} \\
P(C^C) &= \frac{1}{30} \\

&=> \\

P(C) &= 1 - P(C^C) = 1 - \frac{1}{30} = \frac{29}{30} _\square
\end{align}
```

##### <a name="7.b.4"></a> 7.b.4. $D=\{\text{haya exactamente una mujer entre las 3 personas elegidas.}\}$

Se puede calcular con combinatorios eligiendo congreso y persona:

```math
\begin{align}
P(D) &= \frac{\text{casos\_positivos}_D}{\text{casos\_totales}} \\
P(D) &= \frac{\begin{pmatrix} 3 \\ 1 \end{pmatrix} \times \begin{pmatrix} 6 \\ 1 \end{pmatrix} \times \begin{pmatrix} 2 \\ 2 \end{pmatrix} \times \begin{pmatrix} 4 \\ 2 \end{pmatrix}}{10 \times 9 \times 8} \\
P(D) &= \frac{\frac{3!}{1! \times 2!} \times \frac{6!}{1! \times 5!} \times \frac{2!}{2! \times 0!} \times \frac{4!}{2! \times 2!}}{10 \times 9 \times 8} \\
P(D) &= \frac{3 \times 6 \times 1 \times 6}{10 \times 9 \times 8} \\
P(D) &= \frac{3 \times 2 \times 3 \times 2 \times 3}{2 \times 5 \times 3 \times 3 \times 2^{3}} \\
P(D) &= \frac{2^{2} \times 3^{3}}{2^{4} \times 3^{2} \times 5} \\
P(D) &= \frac{3}{2^{2} \times 5} \\
P(D) &= \frac{3}{20} _\square
\end{align}
```

> [Volver](../README.md)
