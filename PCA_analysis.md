# Análisis de Componentes Principales (PCA) aplicado a Genómica

Este documento detalla el uso del método **PCA** para la reducción de dimensionalidad de los datos de expresión génica (RNA-seq) de 5 tipos de tumores del TCGA.

## 1. Justificación del Método
El conjunto de datos original contiene más de 20,000 genes por paciente. El PCA es un método **lineal y paramétrico** que nos permite:
* **Simplificar la complejidad:** Reducir miles de dimensiones a 2 o 3 componentes principales.
* **Eliminar ruido:** Ignorar variaciones pequeñas que no ayudan a distinguir los tumores.
* **Visualizar clústeres:** Observar si los pacientes con el mismo diagnóstico (ej. BRCA) se agrupan de forma natural.

## 2. Flujo de Trabajo (Workflow)

Para ejecutar este análisis, seguimos estos pasos en el script de R:

### A. Preprocesamiento
Antes de aplicar el modelo, es vital limpiar los datos:
1. **Carga de librerías:** Usamos `stats` para el cálculo y `ggplot2` para el gráfico.
2. **Normalización:** Se utiliza el parámetro `center=TRUE` en la función `prcomp()`. Esto asegura que los genes con valores de expresión muy altos no dominen el análisis por encima de otros.

### B. Ejecución del Modelo
El código clave utilizado es:
```r
# Cálculo del PCA sobre los primeros 500 genes
pca.results <- prcomp(data, center=TRUE, scale.=FALSE)
