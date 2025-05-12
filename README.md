# 📌 Práctica de Algoritmos de Ordenamiento  

## Información General  
- **Título:** Comparación de Tiempos de Algoritmos de Ordenamiento  
- **Asignatura:** Estructura de Datos  
- **Carrera:** Computación  
- **Estudiante:** Jonnathan Saavedra y Pedro Pesántez
- **Fecha:** 11 de mayo del 2025
- **Profesor:** Ing. Pablo Torres  

---

## 🛠️ Descripción  
Esta práctica compara el rendimiento de cinco algoritmos de ordenamiento en Python:  
- **Burbuja**  
- **Burbuja Mejorado**  
- **Selección**  
- **Inserción**  
- **Shell Sort**  

Los tiempos de ejecución se miden en arreglos de distintos tamaños: **5,000, 10,000, 30,000, 50,000 y 100,000 elementos**, generados aleatoriamente. El proyecto está estructurado en tres archivos principales:

### 🔹 `sort_methods.py`  
Contiene la clase encargada de implementar los algoritmos de ordenamiento. Cada método trabaja sobre una copia del arreglo original usando `.copy()` para evitar modificar el conjunto desordenado.

### 🔹 `benchmarking.py`  
Define la clase `Benchmarking`, que crea un arreglo principal con 100,000 números aleatorios y genera subconjuntos a partir de él. También incluye un método para medir tiempos de ejecución con `perf_counter()` para obtener resultados precisos.

### 🔹 `app.py`  
Aquí se instancian las clases anteriores y se ejecutan las pruebas. Se organizan los algoritmos en un diccionario, se generan los arreglos y se grafican los resultados usando `matplotlib.pyplot`, mostrando la relación entre tamaño del arreglo y tiempo de ejecución.

---

## 📈 Metodología  
1. Se generaron arreglos de números aleatorios para cada tamaño de prueba.  
2. Se aplicaron los métodos de ordenamiento sobre los mismos conjuntos de datos.  
3. Se registró el tiempo de ejecución antes y después de cada proceso.  
4. Se utilizó medición precisa para capturar los tiempos de ejecución.  

---

## 🚀 Ejecución  
Para ejecutar el proyecto:  

1. **Ejecutar el script:**  
   
   ```bash  
   python app.py  
---
## 📑 Tabla de Resultados  

| Tamaño del Arreglo | Burbuja    | Burbuja Mejorado | Selección  | Inserción  | Shell         |
|--------------------|------------|------------------|------------|------------|---------------|
| 5,000              | 0.432608s  | 0.647863s         | 0.252903s  | 0.282392s  | **0.006465s** |
| 10,000             | 1.659429s  | 2.519984s         | 1.035079s  | 1.211551s  | **0.016093s** |
| 30,000             | 20.753565s | 42.122268s        | 17.061042s | 19.559468s | **0.094597s** |
| 50,000             | 71.783256s | 115.268520s       | 26.506343s | 30.057701s | **0.109980s** |
| 100,000            | 183.737352s| 281.819681s       | 114.828962s| 131.718439s| **0.250138s** |

## 📊 Gráfica de Comparación y Resultados en el Terminal  
La siguiente imagen muestra la comparación visual de los tiempos de ejecución:  

![Gráfica de Comparación](https://github.com/user-attachments/assets/066e095e-c999-404b-aca2-a61d78c5f60a)

La siguiente imagen muestra los tiempos con cada método en el terminal: 

![Datos de Terminal](https://github.com/user-attachments/assets/0a6bf99f-8f2a-43c7-bead-677090ae178d)  

---

## 🔍 Análisis y Conclusiones  
#### Conclusiones Jonnathan Saavedra:
**Burbuja**

El algoritmo de ordenamiento por burbuja tiene una complejidad temporal de O(n²) en el peor caso, debido a la necesidad de realizar n - 1 pasadas completas sobre el arreglo y comparar pares adyacentes en cada iteración. Aunque es intuitivo y fácil de implementar, su rendimiento decrece considerablemente en conjuntos de datos grandes debido al alto número de comparaciones e intercambios.

**Burbuja Mejorado**

Esta variante introduce una condición de parada basada en la ausencia de intercambios, lo que permite reducir iteraciones innecesarias cuando el arreglo ya está parcialmente ordenado. Sin embargo, su peor caso sigue siendo O(n²), y en esta prueba experimental mostró tiempos superiores al método estándar, lo que sugiere que la optimización aplicada no tuvo el impacto esperado en conjuntos aleatorios.

**Selección**

El ordenamiento por selección tiene una complejidad de O(n²) en todos los casos, ya que siempre realiza n - 1 búsquedas del mínimo, independientemente del estado inicial del arreglo. Aunque requiere menos intercambios que el método burbuja, su número de comparaciones sigue siendo alto, lo que limita su eficiencia en arreglos de gran tamaño.

**Inserción**

El algoritmo de inserción tiene una complejidad de O(n²) en el peor caso, cuando los datos están completamente desordenados y cada elemento debe desplazarse hasta su posición correcta en el subarreglo ordenado. Sin embargo, en el mejor caso, cuando el arreglo ya está ordenado o casi ordenado, su complejidad se reduce a O(n), lo que lo hace una opción eficiente para conjuntos de datos parcialmente ordenados.

**Shell Sort**

El algoritmo Shell Sort es una optimización del método de inserción que utiliza una secuencia de incrementos para comparar y mover elementos distantes antes de aplicar el ordenamiento final. Su complejidad varía dependiendo de la secuencia utilizada, pero en la práctica suele estar en el rango de O(n log n). Debido a la reducción progresiva del intervalo de comparación, este método logra tiempos de ejecución significativamente menores en comparación con los algoritmos de O(n²), lo que lo convierte en la opción más eficiente en esta prueba.

#### Conclusiones Pedro Pesántez:
Los resultados evidencian cómo la eficiencia de los algoritmos se ve afectada por su complejidad al aumentar el tamaño de los arreglos. Aquellos con complejidad O(n²) presentan una disminución considerable en su rendimiento, mientras que Shell Sort, con una complejidad aproximada a O(n log n), logra mantener tiempos de ejecución bajos y consistentes.

- **Burbuja (O(n²))**
Se posicionó como el menos eficiente. A medida que crece el número de elementos, su rendimiento se deteriora notablemente. Con 100,000 elementos, el tiempo fue de 5 minutos y 17 segundos, lo que evidencia que no es adecuado para datos de gran tamaño.

- **Burbuja Mejorado (O(n²))**
Lejos de mejorar, presentó un rendimiento incluso más pobre. Con el mismo número de elementos, alcanzó un tiempo de 8 minutos y 41 segundos, indicando que la supuesta optimización no tuvo efecto positivo en esta prueba.

- **Selección (O(n²))**
Mostró un rendimiento aceptable solo en tamaños pequeños. Con 100,000 elementos, necesitó 3 minutos y 21 segundos. Aunque más rápido que Burbuja Mejorado, sigue siendo ineficiente en grandes volúmenes.

- **Inserción (O(n²))**
Su comportamiento fue parecido al de Selección. En volúmenes pequeños fue competitivo, pero con 100,000 elementos tardó 3 minutos y 47 segundos, reflejando su limitada escalabilidad.

- **Shell Sort (O(n log n))**
Se destacó como el más rápido y estable. Para 100,000 elementos, el tiempo fue de solo 0.41 segundos, demostrando su capacidad para trabajar eficientemente con grandes conjuntos de datos gracias a su uso de incrementos decrecientes.

En resumen, los algoritmos con complejidad cuadrática no son adecuados para manejar grandes cantidades de datos, mientras que Shell Sort se presenta como una opción mucho más efectiva. Elegir correctamente el algoritmo puede marcar una gran diferencia en cuanto a rendimiento y eficiencia del sistema.
