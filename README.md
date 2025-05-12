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
Esta práctica evalúa el rendimiento de cinco algoritmos de ordenamiento en Python:  
- **Burbuja**  
- **Burbuja Mejorado**  
- **Selección**  
- **Inserción**  
- **Shell**  

Se compararon los tiempos de ejecución en arreglos de distintos tamaños: **5,000, 10,000, 30,000, 50,000 y 100,000 elementos**, generados aleatoriamente.

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

| Tamaño del Arreglo | Burbuja | Burbuja Mejorado | Selección | Inserción | Shell |
|--------------------|---------|------------------|-----------|-----------|--------|
| 5,000 | 0.430512s | 0.616050s | 0.268379s | 0.281681s | **0.006449s** |
| 10,000 | 1.666225s | 2.629890s | 1.039316s | 1.086095s | **0.014736s** |
| 30,000 | 23.874193s | 41.591046s | 16.807832s | 19.298807s | **0.094822s** |
| 50,000 | 70.633919s | 120.358601s | 31.222073s | 29.222461s | **0.111307s** |
| 100,000 | 176.253780s | 276.323302s | 114.346911s | 138.392213s | **0.442078s** |

## 📊 Gráfica de Comparación  
La siguiente imagen muestra la comparación visual de los tiempos de ejecución:  

![Gráfica de Comparación](https://github.com/user-attachments/assets/9e731f31-d567-427a-a5be-1143d1b764b3)  

---

## 🔍 Análisis y Conclusiones  
#### Conclusiones Jonnathan Saavedra:
- **Shell Sort** es el más eficiente para todos los tamaños de arreglos, con tiempos de ejecución significativamente menores.  
- **Burbuja Mejorado** tuvo tiempos más altos que **Burbuja estándar**, lo cual sugiere que la optimización introducida no fue beneficiosa en este caso específico.  
- **Selección e Inserción** muestran tiempos similares en arreglos pequeños, pero **Selección** se vuelve más eficiente con tamaños más grandes.  
- **Burbuja estándar** confirma su ineficiencia en comparación con otros métodos más avanzados.  
#### Conclusiones Pedro Pesántez:
- **Shell Sort** fue el más eficiente en todos los casos, reduciendo el tiempo de ejecución gracias a su estrategia de múltiples incrementos.  
- **Burbuja Mejorado** no superó a Burbuja estándar, lo que indica que su optimización no fue efectiva en este conjunto de pruebas.  
- **Selección** mostró tiempos competitivos en arreglos pequeños, pero su desempeño disminuyó en conjuntos más grandes debido a su número fijo de comparaciones.  
- **Inserción** es eficiente para datos casi ordenados, pero su rendimiento empeora conforme aumenta el tamaño del arreglo.  
- **Burbuja estándar** tuvo los peores tiempos, confirmando su ineficiencia para volúmenes grandes debido a su alta complejidad computacional.  

Los resultados evidencian cómo la eficiencia de los algoritmos se ve afectada por su complejidad al aumentar el tamaño de los arreglos. Aquellos con complejidad O(n²) presentan una disminución considerable en su rendimiento, mientras que Shell Sort, con una complejidad aproximada a O(n log n), logra mantener tiempos de ejecución bajos y consistentes.

**Burbuja (O(n²))**
Se posicionó como el menos eficiente. A medida que crece el número de elementos, su rendimiento se deteriora notablemente. Con 100,000 elementos, el tiempo fue de 5 minutos y 17 segundos, lo que evidencia que no es adecuado para datos de gran tamaño.

**Burbuja Mejorado (O(n²))**
Lejos de mejorar, presentó un rendimiento incluso más pobre. Con el mismo número de elementos, alcanzó un tiempo de 8 minutos y 41 segundos, indicando que la supuesta optimización no tuvo efecto positivo en esta prueba.

**Selección (O(n²))**
Mostró un rendimiento aceptable solo en tamaños pequeños. Con 100,000 elementos, necesitó 3 minutos y 21 segundos. Aunque más rápido que Burbuja Mejorado, sigue siendo ineficiente en grandes volúmenes.

**Inserción (O(n²))**
Su comportamiento fue parecido al de Selección. En volúmenes pequeños fue competitivo, pero con 100,000 elementos tardó 3 minutos y 47 segundos, reflejando su limitada escalabilidad.

**Shell Sort (O(n log n))**
Se destacó como el más rápido y estable. Para 100,000 elementos, el tiempo fue de solo 0.41 segundos, demostrando su capacidad para trabajar eficientemente con grandes conjuntos de datos gracias a su uso de incrementos decrecientes.

En resumen, los algoritmos con complejidad cuadrática no son adecuados para manejar grandes cantidades de datos, mientras que Shell Sort se presenta como una opción mucho más efectiva. Elegir correctamente el algoritmo puede marcar una gran diferencia en cuanto a rendimiento y eficiencia del sistema.
