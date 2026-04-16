# Cancer-Dimensionality-Reduction

Este proyecto aplica técnicas de aprendizaje no supervisado para explorar y visualizar la estructura de datos de expresión génica provenientes de **The Cancer Genome Atlas (TCGA)**. El objetivo principal es evaluar cómo diferentes modelos de reducción de dimensionalidad logran agrupar las muestras según su tipo de tumor original.

## Descripción general

El análisis de datos transcriptómicos de tumores permite identificar patrones biológicos complejos y relaciones entre muestras que no siempre son evidentes en espacios de alta dimensionalidad. En este repositorio se utilizan métodos de reducción de dimensionalidad para estudiar si los perfiles de expresión génica conservan información suficiente para discriminar distintos tipos tumorales.

Los cinco tipos de cáncer incluidos en este análisis son:

- **BRCA**: Breast Invasive Carcinoma  
- **KIRC**: Kidney Renal Clear Cell Carcinoma  
- **COAD**: Colon Adenocarcinoma  
- **LUAD**: Lung Adenocarcinoma  
- **PRAD**: Prostate Adenocarcinoma  

Estos tumores fueron seleccionados porque representan entidades biológicas bien definidas y con mecanismos moleculares diferentes, lo que los convierte en un buen modelo para evaluar el desempeño de técnicas de agrupamiento y visualización en datos ómicos.

## Fundamento biológico de los tumores analizados

### 1. BRCA — Breast Invasive Carcinoma
El carcinoma invasor de mama es un grupo tumoral heterogéneo que incluye subtipos moleculares con perfiles transcriptómicos diferentes, como luminal, HER2 positivo y triple negativo. Entre sus principales mecanismos de señalización se encuentran:

- **Receptor de estrógeno (ER)** en tumores luminales
- **HER2/ERBB2** en tumores HER2 positivos
- **PI3K–AKT–mTOR**
- **MAPK**
- Alteraciones en **TP53** y reparación del ADN, especialmente en tumores más agresivos

Estas diferencias moleculares impactan directamente en los patrones de expresión génica y favorecen su separación en análisis no supervisados.

### 2. KIRC — Kidney Renal Clear Cell Carcinoma
El carcinoma renal de células claras se caracteriza por la alteración del gen **VHL**, lo que genera estabilización de los factores inducibles por hipoxia (**HIF-1α/HIF-2α**) y una activación sostenida de genes relacionados con angiogénesis y metabolismo tumoral. Sus principales vías incluyen:

- **VHL–HIF**
- **VEGF** y angiogénesis
- **PI3K–AKT–mTOR**
- Reprogramación metabólica tumoral

Este perfil molecular confiere a KIRC una identidad biológica muy particular, frecuentemente distinguible en estudios transcriptómicos.

### 3. COAD — Colon Adenocarcinoma
El adenocarcinoma de colon presenta como eje central la activación de la vía **Wnt/β-catenina**, generalmente asociada a alteraciones en **APC**. Además, en su progresión participan otras vías relevantes:

- **Wnt/β-catenina**
- **EGFR / RAS / RAF / MEK / ERK**
- **PI3K–AKT**
- **TGF-β**
- **NF-κB**
- **Notch**

La combinación de proliferación, inflamación y alteraciones en diferenciación celular genera perfiles de expresión distintivos.

### 4. LUAD — Lung Adenocarcinoma
El adenocarcinoma de pulmón es uno de los tumores con mayor diversidad de drivers oncogénicos. Entre las alteraciones más frecuentes se encuentran mutaciones o fusiones en genes como **EGFR, KRAS, ALK, ROS1, RET, BRAF** y **MET**. Las principales vías de señalización son:

- **RTK–RAS–RAF–MEK–ERK**
- **PI3K–AKT–mTOR**
- Señalización mediada por **EGFR**
- Vías asociadas a proliferación, supervivencia y resistencia terapéutica

Debido a esta diversidad molecular, LUAD constituye un excelente modelo para evaluar heterogeneidad transcriptómica.

### 5. PRAD — Prostate Adenocarcinoma
El adenocarcinoma de próstata depende en gran medida de la señalización del **receptor androgénico (AR)**, que regula proliferación y supervivencia tumoral. También se observan alteraciones frecuentes en:

- **AR (androgen receptor)**
- **PI3K–AKT–mTOR**
- **PTEN**
- **TMPRSS2–ERG**
- **Wnt/β-catenina**
- **MAPK**

La interacción entre la vía androgénica y otras redes de señalización contribuye a la progresión tumoral y a la aparición de resistencia terapéutica.

## Relevancia para la reducción de dimensionalidad

Las diferencias en señalización celular, regulación transcripcional y programas biológicos entre BRCA, KIRC, COAD, LUAD y PRAD generan patrones de expresión génica característicos. Por ello, estos tumores representan una base adecuada para poner a prueba algoritmos de reducción de dimensionalidad como PCA, t-SNE o UMAP.

El supuesto central del proyecto es que, si los métodos empleados preservan adecuadamente la estructura de los datos, entonces las muestras deberían tender a agruparse de acuerdo con su identidad tumoral original. De este modo, la reducción de dimensionalidad no solo actúa como herramienta de visualización, sino también como estrategia exploratoria para detectar similitudes, separaciones biológicas y heterogeneidad intratumoral.

## Objetivos del proyecto

- Explorar datos de expresión génica de distintos tumores de TCGA
- Reducir la dimensionalidad de matrices de alta complejidad
- Visualizar agrupamientos naturales entre muestras
- Comparar el desempeño de distintos métodos no supervisados
- Relacionar los patrones observados con la biología molecular de cada tipo tumoral

## Posibles aplicaciones

- Exploración de heterogeneidad tumoral
- Identificación visual de subgrupos moleculares
- Evaluación preliminar de separabilidad entre clases tumorales
- Apoyo a análisis posteriores de clustering o clasificación

## Fuente de datos

Los datos utilizados provienen de **The Cancer Genome Atlas (TCGA)**, un repositorio ampliamente utilizado en investigación oncológica para el estudio integrado de genómica, transcriptómica y otras capas moleculares de múltiples tipos de cáncer.


## Contexto biológico de los datos

Los datos analizados en este proyecto corresponden a perfiles de expresión génica derivados de muestras tumorales. Cada muestra contiene información sobre la actividad de miles de genes, lo que permite caracterizar el comportamiento molecular de distintos tipos de cáncer.

Las diferencias en la expresión génica entre tumores reflejan alteraciones en procesos biológicos clave como:

- **Proliferación celular**  
- **Angiogénesis**  
- **Metabolismo tumoral**  
- **Respuesta inmune**  

Estas variaciones generan firmas transcriptómicas específicas para cada tipo de tumor, permitiendo su diferenciación en función de su comportamiento biológico y molecular.
## Importancia en el análisis de dimensionalidad

Los datos transcriptómicos presentan una alta dimensionalidad, debido al gran número de genes evaluados simultáneamente. Esto dificulta su interpretación directa.

La aplicación de métodos de reducción de dimensionalidad permite:

- **Simplificar la complejidad de los datos**  
- **Facilitar la visualización de patrones**  
- **Detectar agrupamientos entre muestras**  

Se espera que, si los métodos conservan adecuadamente la información biológica, las muestras se agrupen según su tipo tumoral.

## Consideraciones y limitaciones

- La calidad del análisis depende del preprocesamiento de los datos  
- Existe heterogeneidad biológica dentro de un mismo tipo tumoral  
- Los métodos utilizados son de carácter exploratorio  
- No permiten establecer relaciones causales directas  

Este enfoque permite explorar la biología del cáncer desde una perspectiva integradora, facilitando la interpretación de patrones complejos en datos de alta dimensión.
