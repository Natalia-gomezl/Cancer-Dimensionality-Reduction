# Cancer-Dimensionality-Reduction

Este proyecto aplica técnicas de **aprendizaje no supervisado** para explorar y visualizar la estructura de datos de expresión génica proveniente de **The Cancer Genome Atlas (TCGA)**. El objetivo principal es evaluar cómo diferentes modelos de reducción de dimensionalidad logran agrupar las muestras según su tipo de tumor original.

##  Reducción de Dimensionalidad: Análisis Genómico TCGA
Este proyecto tiene como propósito aplicar técnicas de  aprendizaje no supervisado para reducir la complejidad de datos biológicos masivos (RNA-seq). Trabajamos con muestras de 5 tipos de cáncer para identificar patrones que permitan diferenciarlos visualmente.

##  Objetivos del Proyecto
1. **Implementar** tres métodos de reducción de dimensionalidad: PCA, t-SNE y UMAP.
2. **Analizar** la capacidad de cada algoritmo para agrupar tumores según su expresión génica.
3. **Colaborar** en un entorno profesional utilizando Git y GitHub.

##  Estructura del Repositorio
Para facilitar la navegación, el proyecto se organiza de la siguiente manera:

* **`Data/`**: Contiene los archivos `data.csv` y `labels.csv` con la información genómica.
* **`Scripts/`**: Incluye los códigos fuente ejecutables en R.
* **`Methods/`**: Documentación técnica detallada de cada metodología aplicada.
* **`Results/`**: Carpeta con las visualizaciones y gráficos generados.

## Instrucciones de Uso

### Requisitos
Es necesario tener instalado **R** y las siguientes librerías:
* `ggplot2`
* `stats`

### Ejecución
1. **Cargar los datos**: Asegúrese de que los archivos estén en la carpeta `Data/`.
2. **Ejecutar los scripts**: Los scripts se ubican en la carpeta `Scripts/`. 
   > **Nota:** Asegúrese de ajustar la ruta del directorio de trabajo con el comando `setwd()` antes de correr el análisis.

---


