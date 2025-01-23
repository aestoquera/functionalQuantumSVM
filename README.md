# Comparación entre Algoritmos de Machine Learning Clásicos y Cuánticos

Este proyecto compara el desempeño de algoritmos de Machine Learning clásicos y cuánticos utilizando un dataset de cáncer de mama, explorando diferentes metodologías de Support Vector Machines (SVM) para clasificación. Incluye análisis detallados de preprocesamiento, reducción de dimensionalidad, y benchmarking de métricas como precisión, tiempo de ejecución y número de evaluaciones de circuito cuántico requeridas.

## Contenido del Código

1. **Instalación de dependencias**  
   Las bibliotecas principales utilizadas son:
   - `qiskit` para simulación cuántica.
   - `qiskit_machine_learning` para kernels cuánticos.
   - `pennylane` para modelos cuánticos variacionales.
   - `scikit-learn` para preprocesamiento y SVM clásicos.

2. **Carga y Preprocesamiento del Dataset**  
   - Uso del dataset de cáncer de mama de `sklearn`.
   - Análisis exploratorio y eliminación de características altamente correlacionadas.
   - Divisiones de entrenamiento y prueba.
   - Reducción de dimensionalidad mediante PCA.

3. **Implementaciones de Algoritmos**  
   - **SVM Clásico:** Implementación con el kernel RBF.
   - **SVM con Kernel Cuántico:**  
     Entrenamiento y predicción con una matriz de kernel cuántico basada en `pennylane`.
   - **SVM Cuántico Variacional:**  
     Entrenamiento con modelos cuánticos variacionales optimizados con `AdamOptimizer`, evitando el cálculo explícito de matrices de kernel.
   - **SVM Clásico Simple:** Implementación manual con kernel polinómico.

4. **Benchmarking y Comparación**  
   - Comparación de precisión y tiempos de entrenamiento entre modelos clásicos y cuánticos.
   - Análisis del número de evaluaciones requeridas por circuitos cuánticos para kernels y modelos variacionales.
   - Uso de datos sintéticos para simular escenarios a gran escala.

5. **Visualización de Resultados**  
   - Gráficas de precisión y tiempos de ejecución en función del tamaño del dataset.
   - Comparaciones logarítmicas entre modelos cuánticos y clásicos.

## Requisitos

Instalar las dependencias necesarias con los siguientes comandos:

```bash
pip install qiskit==0.32.1
pip install qiskit-aer
pip install qiskit_machine_learning
pip install pennylane
pip install imbalanced-learn
```
## Ejecución
Descarga el código y ejecuta las celdas de manera secuencial.
Asegúrate de tener configurado un entorno compatible con qiskit y pennylane.
Revisa las gráficas generadas para comprender la comparación de modelos.
## Notas Adicionales
Limitaciones Cuánticas: Algunos enfoques cuánticos, como el SVM basado en kernel cuántico, son computacionalmente costosos debido al cálculo explícito de matrices de kernel.
Optimización Variacional: Los modelos variacionales son más eficientes en problemas a gran escala, ya que no requieren calcular todas las interacciones entre datos.
## Créditos
Este proyecto fue desarrollado como una exploración comparativa entre modelos clásicos y cuánticos de Machine Learning, aprovechando herramientas modernas como Qiskit y Pennylane
