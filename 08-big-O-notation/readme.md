# Entendiendo el funcionamiento del Big O Notation: Una guía para analizar la eficiencia de algoritmos

## ¿Qué es el Big O Notation?

El Big O Notation es una notación matemática utilizada para describir el comportamiento asintótico de una función en términos de su crecimiento o complejidad. 
En el contexto de la informática, se aplica para analizar el tiempo de ejecución y el uso de recursos de un algoritmo a medida que aumenta el tamaño de entrada.

El término "O" en "Big O" se refiere a "Orden de". Cuando decimos que un algoritmo tiene una complejidad de O(f(n)), estamos indicando que el tiempo de ejecución o 
la cantidad de recursos utilizados por el algoritmo crece en el mismo orden que la función f(n). Aquí, "n" representa el tamaño de la entrada del algoritmo.


## ¿Por qué es importante el Big O Notation?

El Big O Notation nos permite comparar la eficiencia de dos algoritmos sin preocuparnos por detalles específicos del hardware o el lenguaje de programación utilizado. Es una herramienta fundamental para los desarrolladores, ya que les permite tomar decisiones informadas sobre qué algoritmo utilizar en función de los requerimientos y restricciones del proyecto.

Además, al evaluar la complejidad de un algoritmo, el Big O Notation nos ayuda a identificar posibles cuellos de botella y puntos débiles, lo que puede conducir a optimizaciones y mejoras en el rendimiento.

## Ejemplos de Big O Notation

Existen varios tipos de complejidades comunes que se expresan a través del Big O Notation:

### O(1) - Tiempo constante:
Tiempo constante: El tiempo de ejecución del algoritmo no depende del tamaño de la entrada. Es decir, el algoritmo toma la misma cantidad de tiempo independientemente de cuántos elementos procese. Un ejemplo es el acceso a un elemento en un arreglo por su índice.

```javascript
function accessFirstElement(arr) {
  return arr[0]; // Acceso al primer elemento del arreglo
}
```

### O(log n) - Tiempo logarítmico:
Tiempo logarítmico: El tiempo de ejecución del algoritmo aumenta de manera logarítmica con el tamaño de la entrada. Este tipo de complejidad es común en algoritmos de búsqueda binaria.

```javascript
function binarySearch(arr, target) {
  let left = 0;
  let right = arr.length - 1;

  while (left <= right) {
    const mid = Math.floor((left + right) / 2);
    if (arr[mid] === target) return mid;
    if (arr[mid] < target) left = mid + 1;
    else right = mid - 1;
  }

  return -1; // Elemento no encontrado
}
```

### O(n) - Tiempo lineal:
Tiempo lineal: El tiempo de ejecución del algoritmo crece linealmente con el tamaño de la entrada. Un ejemplo es recorrer una lista o arreglo.

```javascript
function sumArrayElements(arr) {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum += arr[i];
  }
  return sum;
}
```

### O(n log n) - Tiempo log-lineal:
Tiempo log-lineal: Se encuentra comúnmente en algoritmos de ordenación eficientes, como el algoritmo de ordenación rápida (QuickSort) y el algoritmo de mezcla (MergeSort).

```javascript
function mergeSort(arr) {
  if (arr.length <= 1) return arr;

  const mid = Math.floor(arr.length / 2);
  const left = arr.slice(0, mid);
  const right = arr.slice(mid);

  return merge(mergeSort(left), mergeSort(right));
}

function merge(left, right) {
  let result = [];
  let leftIndex = 0;
  let rightIndex = 0;

  while (leftIndex < left.length && rightIndex < right.length) {
    if (left[leftIndex] < right[rightIndex]) {
      result.push(left[leftIndex]);
      leftIndex++;
    } else {
      result.push(right[rightIndex]);
      rightIndex++;
    }
  }

  return result.concat(left.slice(leftIndex)).concat(right.slice(rightIndex));
}
```

### O(n^2) - Tiempo cuadrático:
Tiempo cuadrático: El tiempo de ejecución del algoritmo es proporcional al cuadrado del tamaño de la entrada. Suelen ser algoritmos con bucles anidados.

```javascript
function swap(arr, posicion1, posicion2){
    let temp = arr[posicion1];
    arr[posicion1] = arr[posicion2];
    arr[posicion2] = temp;
}

function burbuja(arr){
    let i, j;
    for( i = 0; i < arr.length; i++){
        console.log('---------------------------');
        for (j = 0; j < arr.length - i -1; j++) {
            console.log(arr);
            if(arr[j] > arr[j+1]){
                swap(arr,j,j+1)
            }
        }
    }
    return arr;
}
let array = [8,4,6,2,1];
console.log(burbuja(array));
```

Es importante recordar que estos ejemplos ilustran la complejidad temporal de los algoritmos para propósitos educativos y de demostración. En la práctica, la elección del algoritmo adecuado dependerá del contexto específico y las características del problema que se esté resolviendo. Al utilizar el Big O Notation, los desarrolladores pueden tomar decisiones informadas para asegurarse de que sus algoritmos sean eficientes y escalables.
