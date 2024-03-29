### <a name="2.a"></a> 2.a. De un grupo de 35 deportistas se necesita elegir 5 para participar de una competición. ¿De cuántas formas distintas puede hacerse? ¿Qué cambia si esos cinco representantes a su vez cumplen cinco funciones distintas?

En la primer pregunta nos están pidiendo que contemos los distintos conjuntos (sin orden) que contengan 5 deportistas de los 35 totales. Como sus funciones son equivalentes, no importa el orden, cada uno puede realizar la misma tarea que otro y reemplazarlo facilmente.

Por lo tanto, para el primer lugar en el quinteto tenemos 35 opciones, para el segundo 34, y así con los 5 lugares:

```math
35 \times 34 \times 33 \times 32 \times 31
```

Pero veamos lo siguiente, si los 35 deportistas los identificamos como:

```math
\{ D_{i} | i \in [1 .. 35] \}
```

Tenemos que:

```math
\begin{array}{cc}
    \{ D_1, D_2, D_3, D_4, D_5 \} && \{ D_5, D_4, D_3, D_2, D_1 \}
\end{array}
```

Son dos quintetos posibles, pero como hemos dicho, los integrantes cumplen la misma función, por lo que el orden no importa. Debemos considerar una única vez cada subconjunto que contenga los mismos integrantes. Llamamos permutaciones a las distintas combinaciones que se pueden obtener al reordenar los elementos. En nuestro caso, precisamente lo que queremos es no considerar dichas permutaciones, es decir, eliminarlas del conteo total.

Para esto necesitamos conocer cuantas permutaciones son posibles para cada subconjunto de 5 deportistas. Es decir, si ahora restrinjo mi espacio muestral a los 5 deportistas del 1 al 5, cuantos grupos ordenados obtengo. Esto ya lo sabemos hacer:

```math
5 \times 4 \times 3 \times 2 \times 1 = 5!
```

Ahora debemos quitar las permutaciones al resultado total:

```math
\frac{35 \times 34 \times 33 \times 32 \times 31}{5!} = \frac{35!}{30! \times 5!} _\square
```

Ahora bien, si los deportistas van a tener distintas funciones, sería conveniente poder identificar a cada deportista con el rol que va a cumplir y por el cual sería seleccionado en el quinteto. Si vinculamos cada función a un lugar ordenado en el quinteto (por ejemplo, si pensamos en un equipo de básquet el primero podría ser el jugador base, el segundo el escolta, el tercero el alero, cuarto el ala-pivot y quinto el pivot) ya no da lo mismo el orden de selección de cada $D_i$ dentro del subconjunto. Es decir, ahora las permutaciones son importantes y no deben ser eliminadas del conteo total.

```math
35 \times 34 \times 33 \times 32 \times 31 = \frac{35!}{30!} _\square
```

### <a name="2.b"></a> 2.b Generalizar el ítem anterior para el caso de $n$ deportistas y $k$ representantes.

Si ahora tenemos $n$ deportistas y $k$ representantes elegidos en el subconjunto, si no importa el rol de cada integrante tendríamos:

```math
\frac{Total}{Permutaciones} = \frac{\prod_{i=1}^{n} i}{\prod_{i=1}^{n-k}} \times \frac{1}{k!}= \frac{n!}{(n-k)!} \times \frac{1}{k!} _\square
```

Por otro lado, si cada deportista cumplirá un rol distinto, importa el orden y no eliminamos las permutaciones:

```math
Total = \frac{\prod_{i=1}^{n} i}{\prod_{i=1}^{n-k}} = \frac{n!}{(n-k)!} _\square
```

> [Volver](../README.md)
