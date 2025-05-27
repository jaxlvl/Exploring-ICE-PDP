# Flujos de Trabajo de Orange para PDP e ICE

Esta carpeta contiene los archivos de flujo de trabajo (`.ows`) creados con Orange Data Mining para la exploración y visualización de Gráficos de Dependencia Parcial (PDP) y Gráficos de Expectativa Condicional Individual (ICE).

## Archivos

* **`PDP-ICE-PE.ows`**:
    * Flujo de trabajo principal de Orange utilizado en el estudio.
    * Este flujo carga el dataset principal (`White-wine-quality.csv`), entrena modelos de Machine Learning (Árbol de Decisión, Random Forest, SVM) y utiliza el widget `ICE` para generar y visualizar los gráficos PDP, ICE y c-ICE.
    * También incluye componentes para la visualización de la importancia de características y la estructura de los árboles.
    * Está preparado para poder comparar los resultados con otros dos datasets (`student-mat.csv` y `food-nutrition-info.csv`). Para ello tan solo sería necesario desconectar del widget `Data Table` la entrada de un dataset y conectar otro.

## Uso

1.  Para abrir este flujo de trabajo, necesitas tener instalado [Orange Data Mining](https://orangedatamining.com/).
2.  Descarga el archivo `PDP-ICE-PE.ows` y ábrelo con Orange.
3.  **Nota sobre los datasets**: El flujo de trabajo está configurado para buscar los archivos de datos (ej. `White-wine-quality.csv`) en rutas relativas. Si has clonado el repositorio completo, Orange debería poder encontrarlos en la carpeta `../DataBases/`.
    * Si Orange no puede cargar un dataset automáticamente, haz doble clic en el widget `File` correspondiente dentro del flujo de Orange y navega manualmente hasta la ubicación del archivo CSV en la carpeta `DataBases/` de este repositorio.

Este flujo de trabajo permite una exploración interactiva y visual de los conceptos de interpretabilidad discutidos en el proyecto.
