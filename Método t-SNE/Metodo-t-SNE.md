Metodologia t-SNE
================
Silvia M. Pierotti
14/04/2026

**Descripción** La técnica t-Distributed Stochastic Neighbor Embedding
(t-SNE) es uno de un algoritmo de aprendizaje no supervisado para la
visualización de datos de alta dimensionalidad.

En términos sencillos: toma un conjunto de datos de alta dimensionalidad
y lo proyecta en uno de dimensionalidad reducida, intentando que los
puntos que eran parecidos originalmente sigan estando juntos.

**puntos clave:**

*1. El objetivo principal:* A diferencia de otras técnicas como PCA
(Análisis de Componentes Principales), que busca preservar la varianza
global, t-SNE se centra en preservar la estructura local. Esto significa
que es excelente para revelar “clusters” o grupos naturales dentro de
los datos que otras técnicas no ven.

*2. Procedimiento:*

Sobre el espacio de alta dimensión el algoritmo mide la similitud entre
pares de puntos muestrales (i-j) calculando la probabilidad de que un
punto i tenga a j como su vecino. sobre el espacio de baja dimensión
t-SNE intenta recrear esas mismas probabilidades de vecindad utilizando
la distribución t-Student.

*3. Visualizacion de clusters:*

La tecnica conserva los puntos que estan mas cercanos en el espacio
original como vecinos en el espacio de dimensiones reducidas.
Priorizando así estructuras locales (Clusters) ante las estructuras
globales (distancias entre grupos).

*4. Caracteristicas importantes:*

No es lineal: A diferencia de PCA, puede capturar estructuras
extremadamente complejas y curvas.

Perplejidad (Perplexity): Es el parámetro principal. Define cuántos
vecinos cercanos debe considerar el algoritmo. Un valor muy bajo crea
grupos pequeños y aislados; un valor muy alto puede mezclarlo todo.
