### <a name="5"></a> 5. De una caja que contiene 123 bolillas numeradas de 1 a 123 se extraen cinco bolillas. ¿Cuántos resultados posibles hay si:

### <a name="5.a"></a> 5.a. las bolillas se extraen una a la vez y se descartan después de extraerlas?

Se extraen una a la vez, por lo tanto hay orden. Y como se descartan, las opciones disponibles en cada extracción van disminuyendo de acuerdo a la cantidad extraída. Es decir, si $\Omega$ es el espacio muestral:

```math
(1, 2, 3, 4, 5), (5, 4, 3, 2, 1) \in \Omega \\
(1, 1, 1, 1, 1), (1, 1, 1, 2, 3) \notin \Omega
```

Entonces:

```math
123 \times 122 \times 121 \times 120 \times 119 = \frac{123!}{118!} {}_\square
```

### <a name="5.b"></a> 5.b. las bolillas se extraen una a la vez y se devuelven a la caja después de extraerlas?

Seguimos considerando orden al extraer, pero como ahora se devuelven a la caja luego de la extracción, hay reposición de bolillas, por lo tanto puede haber repetición de las mismas y no disminuye la cantidad de opciones disponibles en cada extracción:

```math
(1, 2, 3, 4, 5), (5, 4, 3, 2, 1) \in \Omega \\
(1, 1, 1, 1, 1), (1, 1, 1, 2, 3) \in \Omega
```

Entonces:

```math
123 \times 123 \times 123 \times 123 \times 123 = 123^{5} {}_\square
```

### <a name="5.c"></a> 5.c. las bolillas se extraen todas juntas?

Ahora las bolillas se extraen todas juntas, por lo tanto no hay orden relativo. Lo que extraemos es un subconjunto del conjunto total en lugar de extraer elementos individuales del conjunto total; en cuyo caso al hacerlo de manera secuencial, generan una $n$-upla ordenada. En un experimento así tampoco tiene sentido considerar reposición, ya que la extracción se realiza en un único paso. Lo que haremos es simular esta situación haciendo una extracción secuencial, sin reposición, y luego eliminar las repeticiones provenientes de considerar la extracción ordenada:

```math
(123 \times 122 \times 121 \times 120 \times 119) \times \frac{1}{5!} = \frac{123!}{118!} \times \frac{1}{5!} = \frac{123!}{118! \times 5!}
```

Esto es lo que se conoce como *número combinatorio*:

```math
\frac{123!}{118! \times 5!} = \begin{pmatrix} 123 \\ 5 \end{pmatrix} _\square
```

> [Volver](../README.md)
