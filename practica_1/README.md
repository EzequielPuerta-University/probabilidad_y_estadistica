# Probabilidad y Estadística (C)

## Práctica 1

### 1. Preliminares

1.
    1. [Se deben pintar los frentes de 10 casas y se dispone de 23 colores distintos de pintura. ¿De cuántas formas puede hacerse? ¿De cuántas formas puede hacer si cada casa debe tener un color distinto?](1_preliminares/ejercicio_1.md#1.a)
    2. [Generalizar el ítem anterior para el caso de $k$ casas y $n$ colores.](1_preliminares/ejercicio_1.md#1.b)
2.
    1. [De un grupo de 35 deportistas se necesita elegir 5 para participar de una competición. ¿De cuántas formas distintas puede hacerse? ¿Qué cambia si esos cinco representantes a su vez cumplen cinco funciones distintas?](1_preliminares/ejercicio_2.md#2.a)
    2. [Generalizar el ítem anterior para el caso de $n$ deportistas y $k$ representantes.](1_preliminares/ejercicio_2.md#2.b)
3. [En el tablero de la figura,](1_preliminares/ejercicio_3.md#3)

![Figura1.1.3](img/1_1_3.png)

[¿cuántas formas hay de llegar desde *A* hasta *B* realizando movimientos hacia abajo y hacia la derecha siguiendo las líneas? ¿Cuántos de esos caminos pasan por $X$? Generalizar para un tablero de tamaño $n \times m$.](1_preliminares/ejercicio_3.md#3)

4. [Una clase tiene 3 estudiantes de Villa Ballester y 4 de Claypole. Se elige de entre ellos un comité de 5 estudiantes. Hallar la cantidad de posibles comités que tienen dos estudiantes de Villa Ballester y tres de Claypole.](1_preliminares/ejercicio_4.md#4)
5. [De una caja que contiene 123 bolillas numeradas de 1 a 123 se extraen cinco bolillas. ¿Cuántos resultados posibles hay si](1_preliminares/ejercicio_5.md#5)
    1. [las bolillas se extraen una a la vez y se descartan después de extraerlas?](1_preliminares/ejercicio_5.md#5.a)
    2. [las bolillas se extraen una a la vez y se devuelven a la caja después de extraerlas?](1_preliminares/ejercicio_5.md#5.b)
    3. [las bolillas se extraen todas juntas?](1_preliminares/ejercicio_5.md#5.c)
6.
    1. [¿Cuántos anagramas de **BIBLIOTECARIA** pueden formarse?](1_preliminares/ejercicio_6.md#6.a)
    2. [¿Y con la condición de que la T esté a la derecha de la C?](1_preliminares/ejercicio_6.md#6.b)
    3. [¿Y con la condición de que la T esté a la derecha de la C y la C a la derecha de la R?](1_preliminares/ejercicio_6.md#6.c)
    4. [¿Y con la condición de que las dos A no estén juntas?](1_preliminares/ejercicio_6.md#6.d)
    5. [¿Y con la condición de que todas las vocales estén juntas?](1_preliminares/ejercicio_6.md#6.e)

### 2. Probabilidad en espacios finitos, equiprobabilidad

1. Se arroja dos veces un dado equilibrado, registrándose los resultados obtenidos.
    1. Definir un espacio muestral $S$ apropiado para este experimento.
    2. Describir el conjunto de elementos del espacio muestral que satisface que:
        - ***$A$***: la suma de los dos números obtenidos es por lo menos 5
        - ***$B$***: el valor obtenido en el primer tiro es superior al obtenido en el segundo
        - ***$C$***: el valor obtenido en el primer tiro es un 4
    3. Calcular las probabilidades de los eventos definidos en 1.ii.
    4. Simular en **R** el experimento de tirar dos veces un dado equilibrado.
    5. Simular 1000 veces en **R** el experimento de tirar dos veces un dado equilibrado y estimar las probabilidades de los sucesos definidos en 1.b.
    6. Describir los siguientes conjuntos:
        1. $A \cap B$
        2. $B \cup C$
        3. $A \cap (B \cup C)$
    7. Calcular las probabilidades de los sucesos definidos en 1.vi
    8. Estimar las probabilidades de los sucesos definidos en 1.vi mediante simulaciones. Comparar con los resultados obtenidos en 1.vii.
2.
    1. Dados dos eventos $A$ y $B$ tales que se conocen $P(A \cup B)$ y $P(A \cap B)$, hallar una fórmula para la probabilidad de que ocurra exactamente uno de estos eventos.
    2. Una compañía constructora trabaja en dos proyectos diferentes. Sea $A$ el evento: “el primero de los proyectos se termina en la fecha del contrato” y definamos análogamente $B$ para el segundo proyecto. Si $P(A \cup B) = 0.9$ y $P(A \cap B) = 0.5$, ¿cuál es la probabilidad de que exactamente un proyecto se termine para la fecha de contrato?
3. Supongamos que cuando una computadora se “cuelga” (no responde), el 75% de las veces se debe a problemas de memoria y el 15% de las veces a problemas de software y que el 15% de las veces se debe a problemas que no son ni de memoria ni de software. Si una computadora se cuelga,
    1. ¿cuál es la probabilidad de que estos dos problemas ocurran simultáneamente?
    2. ¿cuál es la probabilidad de que ocurra un problema de software y no de memoria?
4. De un bolillero que contiene 5 bolillas numeradas 1, 2, 3, 4, 5 se extrae una al azar, sea la número $k$. Se eliminan las bolillas cuyo número es mayor que $k$ de la urna y se hace una segunda extracción al azar entre las bolillas 1 a $k$, sea la número $j$. Se eliminan las bolillas cuyo número es mayor que $j$ de la urna y se hace una tercera extracción al azar entre las bolillas 1 a $j$.
    1. Describir un espacio muestral adecuado para este experimento y determinar el número de elementos que posee.
    2. ¿Es razonable suponer equiprobabilidad en este espacio? ¿Qué probabilidad le asignaría al $(3,2,1)$?
5. Una firma proveedora de software ha ofrecido sus servicios a 3 empresas. Se definen los eventos $A_i$ = {la empresa $i$ realiza una compra a esta firma} , para $i = 1, 2, 3$. Se sabe que:

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

6. Un grupo de 60 alumnos será subdividido al azar en dos divisiones de 30 alumnos cada una. Cinco de esos alumnos son muy amigos.: Alicia, Beto, Carmen, Diego y Eva:
    1. ¿Cuál es la probabilidad de que todos queden en la misma división?
    2. ¿Cuál es la probabilidad de que sólo quede separado Diego?
7. De un grupo de 6 mujeres y 4 hombres se deben elegir 3 personas para que los representen en tres congresos a desarrollarse en mayo, junio y septiembre.
    1. Suponiendo que una persona puede ir a más de un congreso, calcular la probabilidad de que:
        1. a los dos primeros congresos vayan mujeres.
        2. a los dos primeros congresos vayan mujeres y al tercero un hombre.
        3. haya por lo menos una mujer entre las 3 personas elegidas.
    2. Si a cada congreso debe ir una persona diferente, calcular las mismas probabilidades que en (7.i) y además la probabilidad de que haya exactamente una mujer entre las 3 personas elegidas.
8. En un negocio hay 6 productos de cierto tipo, 3 de ellos vencidos y 3 que están dentro del periodo de validez. Si un supervisor, que no sabe cuántos envases válidos o vencidos hay, los revisa, ¿cuál es la probabilidad de que
    1. los tres primeros envases revisados contengan los productos vencidos?
    2. necesite revisar exactamente $i$ envases para encontrar los tres que contienen los productos vencidos? (hacerlo para $i = 4, 5, 6$).
9.
    1. (puede ser útil para el siguiente ítem) Probar que:

        ```math
        P(A_1 \cup A_2 \cup A_3 \cup A_4)=P(A_1) + P(A_2) + P(A_3) + P(A_4) \\
        −P(A_1 \cap A_2) − P(A_1 \cap A_3) − P(A_1 \cap A_4) − P(A_2 \cap A_3) − P(A_2 \cap A_4) − P(A_3 \cap A_4) \\
        + P(A_1 \cap A_2 \cap A_3) + P(A_1 \cap A_2 \cap A_4) + P(A_1 \cap A_3 \cap A_4) + P(A_2 \cap A_3 \cap A_4) \\
        − P(A_1 \cap A_2 \cap A_3 \cap A_4)
        ```

    2. Cuatro matrimonios deciden bailar un tango, eligiendo las mujeres a sus compañeros al azar.
        1. ¿Cuál es la probabilidad de que la mujer $i$ (fijo) elija a su esposo como pareja de baile; $i=1,2,3,4$?
        2. ¿Cuál es la probabilidad de que al menos una mujer elija a su esposo?
    3. Estimar las probabilidades del item 9.ii por medio de una simulación. Compare con los resultados obtenidos en 9.ii.
