### <a name="2.a"></a> 2.a. Dados dos eventos $A$ y $B$ tales que se conocen $P(A \cup B)$ y $P(A \cap B)$, hallar una fórmula para la probabilidad de que ocurra exactamente uno de estos eventos.

Conocemos las siguientes probabilidades:

```math
\begin{align}
    \Gamma &= P(A \cup B) \\
    \Theta &= P(A \cap B)
\end{align}
```

Y queremos calcular la probabilidad de que ocurra $A$ o $B$ pero no ambos en simultáneo. Llamemos a esta probabilidad $\Delta$:

```math
\begin{align}
\Delta &= P(A - A \cap B) + P(B - A \cap B) \\
\Delta &= P(A) - P(A \cap B) + P(B) - P(A \cap B) \\
\Delta &= P(A) + P(B) - 2 \times P(A \cap B) \\
\Delta &= P(A \cup B) + P(A \cap B) - 2 \times P(A \cap B) \\
\Delta &= P(A \cup B) - P(A \cap B)
\end{align}
```

### <a name="2.b"></a> 2.b. Una compañía constructora trabaja en dos proyectos diferentes. Sea $A$ el evento: “el primero de los proyectos se termina en la fecha del contrato” y definamos análogamente $B$ para el segundo proyecto. Si $P(A \cup B) = 0.9$ y $P(A \cap B) = 0.5$, ¿cuál es la probabilidad de que exactamente un proyecto se termine para la fecha de contrato?

Si tenemos que:

```math
\begin{align}
A &= \{ \text{el primero de los proyectos se termina en la fecha del contrato} \} \\
B &= \{ \text{el segundo de los proyectos se termina en la fecha del contrato} \} \\
P(A \cup B) &= 0.9 \\
P(A \cap B) &= 0.5
\end{align}
```

Entonces:

```math
\begin{align}
P(A \oplus B) &= P(A \cup B) - P(A \cap B) \\
P(A \oplus B) &= 0.9 - 0.5 \\
P(A \oplus B) &= 0.4
\end{align}
```

> [Volver](../README.md)
