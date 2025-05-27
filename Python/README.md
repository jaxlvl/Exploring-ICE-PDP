# Scripts de Python para Análisis PDP e ICE

Esta carpeta contiene los scripts de Python desarrollados para el análisis programático de los Gráficos de Dependencia Parcial (PDP) y Gráficos de Expectativa Condicional Individual (ICE).

## Archivos

1.  **`ICE-PDP-demostration.ipynb`**:
    * Un Jupyter Notebook diseñado para ser ejecutado en Google Colaboratory.
    * Implementa el flujo completo de análisis:
        * Carga del dataset `White-wine-quality.csv` directamente desde una URL raw del repositorio de GitHub del proyecto.
        * Preprocesamiento de datos.
        * Entrenamiento de modelos de regresión (Árbol de Decisión, Random Forest).
        * Cálculo y visualización de la importancia de características.
        * Generación y visualización de gráficos PDP (1D y 2D), ICE y c-ICE utilizando `scikit-learn`.
        * Análisis de interacciones.
    * **Cómo usarlo**: Sube este archivo a Google Colab y ejecútalo celda por celda. No requiere la descarga manual del dataset si se ejecuta en Colab con acceso a internet.

2.  **`ICE-PDP-demostration.py`**:
    * Un script de Python estándar, funcionalmente equivalente al notebook `.ipynb`.
    * Está configurado para cargar el dataset `White-wine-quality.csv` desde una ruta local relativa (`../DataBases/White-wine-quality.csv`), asumiendo que el script se ejecuta desde la carpeta `Python-Script/` y la carpeta `DataBases/` está en el nivel superior del repositorio.
    * **Cómo usarlo**: Ejecútalo en un entorno Python local que tenga instaladas las librerías necesarias (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn).
        ```bash
        python3 ICE-PDP-demostration.py
        ```

## Dependencias Principales

Ambos scripts dependen de las siguientes librerías de Python:
* `pandas`
* `numpy`
* `scikit-learn`
* `matplotlib`
* `seaborn`

Consulta la Sección 3.3.2 del informe principal (`doc/Informe-prácticas.pdf`) para más detalles sobre las versiones.
