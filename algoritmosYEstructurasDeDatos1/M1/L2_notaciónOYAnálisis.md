# Notación O y análisis

## Notación O

El impacto se profundiza a medida que crecemos en el problema a resolver, por lo cual, consideraremos a $N$ tendiendo a infinito.

En ese caso, estaremos considerando su comportamiento asintótico. Al momento de identificar diferentes relaciones entre funciones y recursos, podemos agrupar los comportamientos resultantes en **familias de funciones**, dependiendo de su comportamiento asintótico, y les asignaremos un **orden de complejidad O**.

La notación O-grande no toma en cuenta los factores constantes, es decir, ignora si se hace una mejor o peor implementación del algoritmo, además de independizarlo de los datos de entrada del algoritmo.

Como utilidad de aplicar este concepto es encontrar un límite superior del tiempo de ejecución, es decir, el peor caso

## Cota superior asintótica

Cota superior asintótica es otra manera de nombrar a la notación O.

Se ha notado que los algoritmos, ante entradas pequeñas, pueden mostrar una diferencia de eficiencia mínima. En esos casos, no parece lógico realizar un gran esfuerzo por optimizar un algoritmo, ya que el tiempo de ejecución mejorará muy poco con respecto a otro algoritmo más sencillo.

Sin embargo, también se mencionó que esas situaciones no son tan comunes y que, en realidad, se necesitan algoritmos que funcionen eficientemente ante las grandes entradas. Allí, las diferencias en el tiempo de ejecución, entre los algoritmos equivalentes, se hacen mayores. Además, en estos casos, si se requiere realizar un esfuerzo para optimizar los algoritmos.