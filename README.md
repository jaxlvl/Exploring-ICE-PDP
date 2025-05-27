# Análisis de Interpretabilidad de Modelos con PDP e ICE

## Visión General del Proyecto

Este proyecto se centra en la comprensión y aplicación práctica de técnicas clave para la interpretabilidad de modelos de Machine Learning: los Gráficos de Dependencia Parcial (PDP) y los Gráficos de Expectativa Condicional Individual (ICE). El objetivo principal es explorar cómo estas herramientas nos permiten analizar el comportamiento interno de modelos predictivos, tradicionalmente considerados "cajas negras", facilitando así una mayor comprensión de la influencia de las variables en sus predicciones.

A través de ejemplos prácticos con diversos datasets (principalmente "White Wine Quality"), se ilustra la implementación de PDP e ICE utilizando dos entornos complementarios: el software de minería de datos Orange y el lenguaje de programación Python junto con sus librerías especializadas. Se pone especial énfasis en comparar cómo estas visualizaciones se manifiestan en modelos simples como los Árboles de Decisión (caracterizados por sus gráficos escalonados) y en modelos más complejos como los Random Forest (que tienden a producir gráficos más suaves y donde la explicabilidad es aún más crucial).

Este repositorio contiene el informe de prácticas, los datasets utilizados, los flujos de trabajo de Orange y los scripts de Python desarrollados como parte de este estudio.

## Conceptos Clave Cubiertos

* Inteligencia Artificial Explicable (XAI)
* Gráficos de Dependencia Parcial (PDP / Partial Dependence Plots)
* Gráficos de Expectativa Condicional Individual (ICE / Individual Conditional Expectation Plots)
* Gráficos ICE Centrados (c-ICE / centered ICE Plots)
* Gráficos ICE Derivados (d-ICE / derivative ICE Plots) - Mencionados teóricamente.
* Interpretabilidad de modelos de Machine Learning (Árboles de Decisión, Random Forest, SVM).
* Detección de efectos heterogéneos e interacciones entre variables.

## Herramientas y Tecnologías

* **Orange Data Mining (versión 3.38.1)**: Utilizado para la exploración visual, la construcción interactiva de flujos de trabajo y la generación inicial de gráficos PDP/ICE.
* **Python (versión 3.11.5)**: Empleado para la implementación programática, análisis detallado y generación de visualizaciones personalizadas.
    * **Scikit-learn**: Fundamental para el preprocesamiento de datos, entrenamiento de modelos (`DecisionTreeRegressor`, `RandomForestRegressor`) y generación de PDP/ICE (`PartialDependenceDisplay`).
    * **Pandas**: Para la carga y manipulación eficiente de datos tabulares.
    * **NumPy**: Para operaciones numéricas y manejo de arrays.
    * **Matplotlib / Seaborn**: Para la creación y personalización de las visualizaciones estáticas.
* **Google Colab**: Como entorno principal para la ejecución de los notebooks de Python.

## Componentes del Proyecto

1.  **Informe (`doc/Informe-prácticas.pdf`)**:
    * Documento exhaustivo que detalla los fundamentos teóricos de PDP e ICE, la metodología, los experimentos realizados en Orange y Python, la discusión de resultados y las conclusiones del estudio.

2.  **Datasets (`DataBases/`)**:
    * Contiene los archivos CSV utilizados: `White-wine-quality.csv` como foco principal del análisis, y `food-nutrition-info.csv` y `student-mat.csv` para exploraciones adicionales o pruebas comparativas iniciales.

3.  **Análisis en Orange (`Orange/`)**:
    * Incluye el flujo de trabajo `PDP-ICE-PE.ows`, que permite replicar los análisis visuales e interactivos realizados con Orange Data Mining, mostrando la configuración de modelos y la generación de gráficos ICE/PDP.

4.  **Scripts de Python (`Python-Script/`)**:
    * `ICE-PDP-demostration.ipynb`: Notebook diseñado para Google Colab que implementa el análisis completo. Carga el dataset `White-wine-quality.csv` directamente desde la URL raw del archivo en este repositorio de GitHub, realiza el preprocesamiento, entrena los modelos, calcula la importancia de características y genera los gráficos PDP (1D y 2D), ICE y c-ICE.
    * `ICE-PDP-demostration.py`: Script de Python estándar, funcionalmente equivalente al notebook, pero configurado para cargar los datos desde la carpeta local `DataBases/` dentro de la estructura del repositorio.

## Cómo Empezar / Uso

### 1. Entender el Proyecto
* Se recomienda comenzar leyendo el informe completo en `doc/Informe-prácticas.pdf` para una comprensión profunda del contexto teórico, los métodos aplicados y los hallazgos del estudio.

### 2. Explorar en Orange
1.  Asegúrate de tener instalado [Orange Data Mining](https://orangedatamining.com/) (versión 3.38.1 o compatible).
2.  Abre el archivo de flujo de trabajo `Orange/PDP-ICE-PE.ows` con Orange.
3.  **Nota sobre los datasets**: El flujo de trabajo está configurado para usar los datasets. Si Orange no encuentra los archivos CSV automáticamente al abrir el flujo (debido a diferencias en rutas absolutas guardadas por Orange), puede que necesites re-enlazar manualmente los widgets `File` al dataset `White-wine-quality.csv` (u otros) ubicado en la carpeta `DataBases/` dentro de este repositorio.
4.  Ejecuta los flujos y explora interactivamente los widgets y las visualizaciones generadas.

### 3. Ejecutar los Scripts de Python

#### Opción A: Notebook en Google Colab (`ICE-PDP-demostration.ipynb`)
1.  Accede a Google Colab.
2.  Selecciona `Archivo > Subir cuaderno...` y sube el archivo `Python-Script/ICE-PDP-demostration.ipynb`.
3.  Alternativamente, si el repositorio es público, puedes abrirlo directamente en Colab desde GitHub (`Archivo > Abrir cuaderno > GitHub` y pegando la URL del repositorio o del archivo `.ipynb`).
4.  El notebook está configurado para cargar el dataset `White-wine-quality.csv` directamente desde la URL raw del archivo en este repositorio de GitHub. Solo necesitas ejecutar las celdas en orden.

#### Opción B: Script Local (`ICE-PDP-demostration.py`)
1.  Asegúrate de tener Python (versión 3.11.5 o compatible) y las librerías listadas en la Sección 3.3.2 del informe (`doc/Informe-prácticas.pdf`) instaladas en tu entorno (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn).
2.  Clona o descarga este repositorio en tu máquina local.
3.  Desde tu terminal, navega a la carpeta `Python-Script/`.
4.  Ejecuta el script: `python ICE-PDP-demostration.py`.
5.  Este script está diseñado para cargar el dataset `White-wine-quality.csv` desde la carpeta `../DataBases/` (relativa a la ubicación del script).

## Autor

* **Juan Carlos Valera López**

## Licencia

Este proyecto se distribuye bajo la **Apache License 2.0**. Consulta el archivo `LICENSE` para más detalles.

