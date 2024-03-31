### <a name="3"></a> 3. Supongamos que cuando una computadora se “cuelga” (no responde), el 75% de las veces se debe a problemas de memoria y el 15% de las veces a problemas de software y que el 15% de las veces se debe a problemas que no son ni de memoria ni de software. Si una computadora se cuelga,

#### <a name="3.a"></a> 3.a. ¿cuál es la probabilidad de que estos dos problemas ocurran simultáneamente?

Defino primero los eventos y probabilidades conocidas:

```math
\begin{align}
M &= \{ \text{Problemas de memoria} \} \\
S &= \{ \text{Problemas de software} \} \\
O &= \{ \text{Problemas de otro tipo} \} \\
P(M) &= 0.75 \\
P(S) &= 0.15 \\
P(O) &= 0.15
\end{align}
```

Quiero averigüar:

```math
\begin{align}
P(M \cap S) &= P(M) + P(S) - P(M \cup S) \\
P(M \cap S) &= P(M) + P(S) - (1 - P((M \cup S)^{C})) \\
P(M \cap S) &= P(M) + P(S) - (1 - P(O)) \\
P(M \cap S) &= 0.75 + 0.15 - (1 - 0.15) \\
P(M \cap S) &= 0.05 _\square
\end{align}
```

#### <a name="3.b"></a> 3.b. ¿cuál es la probabilidad de que ocurra un problema de software y no de memoria?

```math
\begin{align}
P(S \cap \neg M) &= P(S) - P(S \cap M) = 0.15 - 0.05 = 0.10 _\square
\end{align}
```

> [Volver](../README.md)
