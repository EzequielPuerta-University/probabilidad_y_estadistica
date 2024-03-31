### <a name="1"></a> 1. Se arroja dos veces un dado equilibrado, registrándose los resultados obtenidos.

### <a name="1.a"></a> 1.a. Definir un espacio muestral $S$ apropiado para este experimento.

Como no se indica nada diferente, supongo que el dado es uno tradicional de 6 caras. Por lo tanto, la tirada del dado puede resultar en cualquier número entre 1 y 6, inclusive. Al estar equilibrado, cada número tiene la misma probabilidad de salir con respecto al resto. Se arroja 2 veces, por lo que hay una secuencia de sucesos y por lo tanto un orden implícito, por lo que nuestro espacio muestral puede ser una tupla cuyo primer coeficiente refleje el resultado de la primer tirada y el segundo coeficiente sea el resultado de la segunda. Defino entonces el espacio muestral $S$ como:

```math
S = \{ (x_1, x_2) | i \in [1, 2], x_i \in [1..6] \}
```

### <a name="1.b"></a> 1.b. Describir el conjunto de elementos del espacio muestral que satisface que:

#### <a name="1.b.1"></a> 1.b.1 ***$A$***: la suma de los dos números obtenidos es por lo menos 5

```math
A = \{ (x_1, x_2) | i \in [1, 2], x_i \in [1..6], \sum_{i=1}^{2} x_i \geq 5 \}
```

#### <a name="1.b.2"></a> 1.b.2. ***$B$***: el valor obtenido en el primer tiro es superior al obtenido en el segundo

```math
B = \{ (x_1, x_2) | x_1 \in [2..6], x_2 \in [1..x_1) \}
```

#### <a name="1.b.3"></a> 1.b.3. ***$C$***: el valor obtenido en el primer tiro es un 4 Definir un espacio muestral $S$ apropiado para este experimento.

```math
C = \{ (4, x_2) | x_2 \in [2..6] \}
```

### <a name="1.c"></a> 1.c. Calcular las probabilidades de los eventos definidos en 1.b.

##### * $P(A)$
Considero $A = S - A^{C}$, con $A^{C}$ como:

```math
\begin{align}
A^{C} &= \{ (x_1, x_2) | i \in [1, 2], x_i \in [1..6], \sum_{i=1}^{2} x_i < 5 \} \\
A^{C} &= \{ (1,1), (1,2), (1,3), (2,1), (2,2), (3,1) \}
\end{align}
```

Por lo tanto:

```math
P(A) = \frac{\text{casos\_positivos}_A}{\text{casos\_totales}} = \frac{\#A}{6 \times 6} = \frac{\#(S - A^{C})}{36} = \frac{30}{36} = \frac{5}{6} _\square
```

##### * P(B)

```math
\begin{align}
B = \{ (2,1), (3,1), (3,2), (4,1), (4,2), (4,3), \\ (5,1), (5,2), (5,3), (5,4), (6,1), (6,2), (6,3), (6,4), (6,5) \} \\
P(B) = \frac{\text{casos\_positivos}_B}{\text{casos\_totales}} = \frac{15}{6 \times 6} = \frac{5}{12} _\square
\end{align}
```

##### * P(C)

```math
\begin{align}
C &= \{ (4,1), (4,2), (4,3), (4,4), (4,5), (4,6) \} \\
P(C) &= \frac{\text{casos\_positivos}_C}{\text{casos\_totales}} = \frac{6}{6 \times 6} = \frac{1}{6} _\square
\end{align}
```

### <a name="1.d"></a> 1.d. Simular en **R** el experimento de tirar dos veces un dado equilibrado.



### <a name="1.e"></a> 1.e. Simular 1000 veces en **R** el experimento de tirar dos veces un dado equilibrado y estimar las probabilidades de los sucesos definidos en 1.b.

### <a name="1.f"></a> 1.f. Describir los siguientes conjuntos:

#### <a name="1.f.1"></a> 1.f.1 $A \cap B$

```math
A \cap B = (S - A^{C}) \cap B = B - (A^{C} \cap B) = B - \{ (2,1), (3,1) \} = \\ \{ (3,2), (4,1), (4,2), (4,3), (5,1), (5,2), (5,3), (5,4), \\ (6,1), (6,2), (6,3), (6,4), (6,5) \} _\square
```

#### <a name="1.f.2"></a> 1.f.2 $B \cup C$

```math
B \cup C = \{ (2,1), (3,1), (3,2), (4,1), (4,2), (4,3), (4,4), (4,5), (4,6) \\ (5,1), (5,2), (5,3), (5,4), (6,1), (6,2), (6,3), (6,4), (6,5) \} _\square
```

#### <a name="1.f.3"></a> 1.f.3 $A \cap (B \cup C)$

```math
A \cap (B \cup C) = \neg A^{C} \cap (B \cup C) = \{ (3,2), (4,1), (4,2), (4,3), (4,4), (4,5), (4,6) \\ (5,1), (5,2), (5,3), (5,4), (6,1), (6,2), (6,3), (6,4), (6,5) \} _\square
```

### <a name="1.g"></a> 1.g. Calcular las probabilidades de los sucesos definidos en 1.f

#### <a name="1.g.1"></a> 1.g.1 $P(A \cap B)$

```math
P(A \cap B) = \frac{\text{casos\_positivos}}{\text{casos\_totales}} = \frac{13}{36} _\square
```

#### <a name="1.g.2"></a> 1.g.2 $P(B \cup C)$

```math
P(B \cup C) = \frac{\text{casos\_positivos}}{\text{casos\_totales}} = \frac{18}{36} = \frac{1}{2} _\square
```

#### <a name="1.g.3"></a> 1.g.3 $P(A \cap (B \cup C))$

```math
P(A \cap (B \cup C)) = \frac{16}{36} = \frac{4}{9} _\square
```

### <a name="1.h"></a> 1.h. Estimar las probabilidades de los sucesos definidos en 1.f mediante simulaciones. Comparar con los resultados obtenidos en 1.g.

> [Volver](../README.md)
