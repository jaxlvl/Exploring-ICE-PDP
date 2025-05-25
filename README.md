# Análisis de Interpretabilidad de Modelos con PDP e ICE

## Visión General del Proyecto

Este proyecto se centra en la comprensión, aplicación y demostración de técnicas de interpretabilidad de modelos de Machine Learning, específicamente los Gráficos de Dependencia Parcial (PDP) y los Gráficos de Expectativa Condicional Individual (ICE). El objetivo es explorar cómo estas herramientas nos permiten "abrir la caja negra" de los modelos predictivos, facilitando la comprensión de su comportamiento y la forma en que las variables influyen en sus predicciones.

A través de ejemplos prácticos, se ilustra la implementación de PDP e ICE utilizando dos entornos principales: el software de minería de datos Orange y el lenguaje de programación Python. Se pone especial énfasis en comparar cómo estas visualizaciones se manifiestan en modelos simples como los Árboles de Decisión (con sus característicos gráficos escalonados) y en modelos más complejos como los Random Forest (donde los gráficos tienden a ser más suaves y la explicabilidad es aún más crucial).

## Conceptos Clave Cubiertos

* Inteligencia Artificial Explicable (XAI)
* Gráficos de Dependencia Parcial (PDP / Partial Dependence Plots)
* Gráficos de Expectativa Condicional Individual (ICE / Individual Conditional Expectation Plots)
* Gráficos ICE Centrados (c-ICE / centered ICE Plots)
* Interpretabilidad de modelos de Machine Learning (Árboles de Decisión, Random Forest, etc.)
* Detección de efectos heterogéneos e interacciones entre variables.

## Herramientas y Tecnologías

* **Orange Data Mining**: Para la exploración visual, construcción de flujos de trabajo y generación interactiva de gráficos PDP/ICE.
* **Python**: Para la implementación programática y análisis detallado.
    * **Scikit-learn**: Para el preprocesamiento de datos, entrenamiento de modelos y generación de PDP/ICE (`PartialDependenceDisplay`).
    * **Pandas**: Para la manipulación de datos.
    * **NumPy**: Para operaciones numéricas.
    * **Matplotlib / Seaborn**: Para la visualización de gráficos.
* **Google Colab**: Como entorno de ejecución para los scripts de Python.
