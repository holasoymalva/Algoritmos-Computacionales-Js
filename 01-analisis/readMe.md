## Introduccion al análisis de algoritmos

El análisis de algoritmos y las estructuras de datos son conceptos clave en la programación y el desarrollo de software. Estos temas nos permiten comprender cómo funcionan los programas que escribimos, y cómo podemos mejorarlos para hacerlos más eficientes en términos de tiempo y espacio. En estos apuntes, abordaremos los conceptos básicos del análisis de algoritmos, incluyendo la notación big O, la complejidad temporal y espacial, y los patrones de resolución de problemas. También exploraremos las diferentes estructuras de datos, como las listas, las pilas, las colas y los árboles, y cómo podemos utilizarlas para resolver problemas específicos de manera eficiente. Al final de estos apuntes, esperamos que tengas una comprensión profunda de estos conceptos y estés listo para aplicarlos a tus propios proyectos de programación.


## Complejidad Computacional [Wiki Reference](https://en.wikipedia.org/wiki/Computational_complexity_theory)


La teoría de la complejidad computacional se enfoca en clasificar los problemas computacionales de acuerdo con su uso de recursos y relacionar estas clases entre sí. Un problema computacional es una tarea resuelta por una computadora. Un problema de cálculo se puede resolver mediante la aplicación mecánica de pasos matemáticos, como un algoritmo .

Un problema se considera intrínsecamente difícil si su solución requiere recursos importantes, sea cual sea el algoritmo utilizado. La teoría formaliza esta intuición, al introducir modelos matemáticos de computación para estudiar estos problemas y cuantificar su complejidad computacional , es decir, la cantidad de recursos necesarios para resolverlos, como el tiempo y el almacenamiento. También se utilizan otras medidas de complejidad, como la cantidad de comunicación (utilizada en la complejidad de la comunicación ), el número de puertas en un circuito (utilizado en la complejidad del circuito ) y el número de procesadores (utilizado en la computación en paralelo).). Uno de los roles de la teoría de la complejidad computacional es determinar los límites prácticos de lo que las computadoras pueden y no pueden hacer. El problema P versus NP , uno de los siete problemas del Premio del Milenio , está dedicado al campo de la complejidad computacional. [1]

Los campos estrechamente relacionados en la informática teórica son el análisis de algoritmos y la teoría de la computabilidad.. Una distinción clave entre el análisis de algoritmos y la teoría de la complejidad computacional es que el primero se dedica a analizar la cantidad de recursos que necesita un algoritmo en particular para resolver un problema, mientras que el segundo hace una pregunta más general sobre todos los algoritmos posibles que podrían usarse para resolver el mismo problema. Más precisamente, la teoría de la complejidad computacional intenta clasificar los problemas que pueden o no pueden resolverse con recursos apropiadamente restringidos. A su vez, imponer restricciones a los recursos disponibles es lo que distingue la complejidad computacional de la teoría de la computabilidad: esta última teoría pregunta qué tipos de problemas pueden, en principio, resolverse algorítmicamente.


## Analisis de algoritmos [Wiki Reference](https://en.wikipedia.org/wiki/Analysis_of_algorithms)

En informática , el análisis de algoritmos es el proceso de encontrar la complejidad computacional de los algoritmos: la cantidad de tiempo, almacenamiento u otros recursos necesarios para ejecutarlos . Por lo general, esto implica determinar una función que relaciona la longitud de la entrada de un algoritmo con el número de pasos que toma (su complejidad temporal ) o el número de ubicaciones de almacenamiento que utiliza (su complejidad espacial ). Se dice que un algoritmo es eficiente cuando los valores de esta función son pequeños o crecen lentamente en comparación con un crecimiento en el tamaño de la entrada. Diferentes entradas de la misma longitud pueden hacer que el algoritmo tenga un comportamiento diferente, por lo queLas descripciones de casos mejores, peores y promedio podrían ser de interés práctico. Cuando no se especifica lo contrario, la función que describe el rendimiento de un algoritmo suele ser un límite superior , determinado a partir de las entradas del peor caso al algoritmo.

## Big O Notation - Notacion de la Gran O

La Notación Big O es una forma de medir el tiempo de ejecución y la complejidad de un algoritmo. Es una notación matemática que se utiliza para describir la relación entre el tamaño del problema y el tiempo que tarda en resolverlo un algoritmo. La Notación Big O se utiliza para describir el límite superior del tiempo de ejecución de un algoritmo y se representa como O(n), donde "n" representa el tamaño del problema.

Aquí hay algunos ejemplos de la Notación Big O en JavaScript:

* Algoritmo de búsqueda lineal: Este algoritmo tiene una complejidad temporal de O(n), ya que debe revisar cada elemento en una secuencia hasta encontrar una coincidencia.

* Algoritmo de búsqueda binaria: Este algoritmo tiene una complejidad temporal de O(log n), ya que divide la secuencia en mitades y descarta la mitad que no contiene el elemento buscado en cada iteración.

* Algoritmo de ordenamiento por selección: Este algoritmo tiene una complejidad temporal de O(n^2), ya que debe comparar cada elemento con todos los demás para encontrar el mínimo y moverlo a su posición final en la secuencia.

* Algoritmo de ordenamiento rápido (QuickSort): Este algoritmo tiene una complejidad temporal de O(n log n) en el mejor y peor de los casos, lo que lo hace mucho más eficiente que el algoritmo de ordenamiento por selección.

Estos son solo algunos ejemplos de la Notación Big O en JavaScript. Al comprender y aplicar esta notación, los programadores pueden mejorar el rendimiento y la eficiencia de sus algoritmos y soluciones de programación.


## Capacidad de Memoria

La capacidad de memoria es un aspecto importante a tener en cuenta en el análisis de algoritmos. Se refiere a la cantidad de memoria que un algoritmo necesita para funcionar adecuadamente.

La cantidad de memoria que un algoritmo utiliza puede afectar su rendimiento y su capacidad para manejar grandes cantidades de datos. Por ejemplo, un algoritmo que utiliza mucha memoria puede ser más lento que otro que utiliza menos memoria, ya que la memoria limita la velocidad de acceso a los datos.

Por lo tanto, es importante tener en cuenta la capacidad de memoria en el análisis de algoritmos para asegurarse de que el algoritmo sea eficiente en términos de memoria y sea capaz de manejar grandes cantidades de datos de manera eficiente.
