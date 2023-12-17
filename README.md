# Implementación de modelos basados en aprendizaje automático para el abordaje de problemas biológicos 2023

En esta carpeta encontrarán los códigos del curso *Implementación de modelos basados en aprendizaje automático para el abordaje de problemas biológicos PEDECIBA 2023*, particularmente los prácticos a mi cargo.

Dentro de las carpetas encontrarán un archivo .ipynb con el práctico correspondiente, además de una carpeta con los datos utilizados y el artículo de donde fueron obtenidos. Los prácticos van aumentando la dificultad a medida que avanzan por lo cual se recomienda la realización secuencial. 

[Información del curso](https://www.pedeciba.edu.uy/es/curso/implementacion-de-modelos-basados-en-aprendizaje-automatico-para-el-abordaje-de-problemas-biologicos/)

## Práctico 0
Dentro de esta carpeta encontrarán un repaso sencillo de Python, mencionamos algunos de los tipos de datos más importante en Python y la realización de  de funciones.
Creamos una función sencilla que permite dividir a la cual le añadimos complejidad a medida que avanza el práctico.

## Práctico 1 | Práctico 2

En esta carpeta encontrarán información relativa al proyecto FlyCellAtlas, que aborda la transcriptómica de célula única en  *Drosophila melanogaster* específicamente los datos de fatbody smart-seq y haltere 10x stringent. Además, se incluye el artículo original, así como una versión completa con una descripción detallada de los métodos utilizados para el análisis de datos de célula única.

### Práctico 1
Durante este práctico comenzamos a familiarizarnos con *Pandas* para el manejo de datos, utilizamos algunas de las aplicaciones más comunes como la selección de columnas específicas, la aplicación de normalización a nuestros datos tanto por medio del método *apply*  de *Pandas* y una función propia, o por medio de los métodos de *sklearn* 

### Práctico 2

Se dividió el práctico 2 en dos archivos .ipynb. 

####  Reducción de dimensionalidad (RD)
En este archivo encontrarán la reducciones de dimensionalidad más comunes. Primero comenzamos haciendo Análisis de Componentes Principales (PCA) por código, luego utilizando *sklearn* y finalmente por medio de *scanpy*, una librería específica para el análisis de datos de célula única.
Luego realizamos la reducción de dimensionalidad por el método tSNE (t-Distributed Stochastic Neighbor Embedding) con *sklearn* y *scanpy*. Finalmente, realizamos el método UMAP (Uniform Manifold Approximation and Projection) sobre nuestros datos con las librerías *scanpy* y *umap-learn*

####  Selección de variables (SV)
Como método de selección de variables sencillo optamos por hacer selección de variables por PCA. Por medio de *sklearn* evaluamos el significado del PCA obtenido al ver la contribución de cada variables (genes) en el mapeo de las células en las nuevas coordenadas. 
Las últimas lineas de código permiten guardar N=100 genes más influyentes en los componentes principales elegidas en un archivo excel. Se recomienda ver el enriquecimiento funcional de GO terms asociados a cada componente o visualizar las interacciones de los genes con *String*. Se observa que cada componente tiene genes enriquecidos para funciones diferentes (no incluido en el archivo). 

## Práctico 3

Durante este práctico analizamos los resultados de pacientes con Chronic Obstructive Pulmonary Disease (COPD) por medio de técnicas de agrupamiento o cluster. 
Se presentan algunas funciones disponibles en *sklearn*. Además enfatiza en la importancia de la normalización y la selección de variables por medio de actividades. 
Se incluyó, posterior a la realización del práctico, un archivo .ipynb con el análisis PCA similar al práctico 2, donde se puede observar la selección de variables de forma más sencilla, junto con la visualización de los pares de componentes por medio de la librería *Seaborn*.

## Práctico 6

Durante este práctico se realiza la predicción de arritmias cardíacas por medio de electrocardiogramas (ECG) de 12 canales y redes convolucionales en una dimensión. 
En este caso los datos y la arquitectura de la red fue obtenida de artículos diferentes. Dentro del archivo .ipynb se referencia la base de datos, y dentro de la carpeta se incluye el artículo donde bue obtenida la arquitectura, con el fin de simplificar el ejercicio se realizó la predicción con sólo una parte de la arquitectura original (Modelo A),
