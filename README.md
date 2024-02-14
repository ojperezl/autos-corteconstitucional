# Autos Corte Constitucional

## Contexto
La Corte Constitucional publica una serie de sentencias judiciales respecto a determinados procesos judiciales. Dichas sentencias sirven de base para futuros procesos, por lo cual son muy relevante para los abogados. Son referentes para establecer los antecedentes de casos similares.

## El problema
No obstante, dichas sentencias vienen listados por orden de emisión y no ofrecen un orden temático. Por esta razón, se presenta una dificultad al momento de revisar los autos de una manera eficiente.

## Solución LLM
El siguiente modelo que sigue en desarrollo, consiste en tomar los archivos PDF en que se publican las sentencias, y a partir de LLMs aplicar técnicas de similitud semántica. De esta manera, el usuario puede ingresar por medio de una frase o palabra la temática que está tratando. Por similitud semántica la presente herramienta encuentra las sentencias que más se acercan al objetivo.

## Estructura del proyecto

### 1. Scrapping
Obtener de la url https://www.corteconstitucional.gov.co/secretaria/autoss/ las sentencias emitidas por la Corte Constitucional.

### 2. Extracción
Extraer el texto de los documentos por bloques de oraciones y consolidar en un único corpus.

### 3. Limpieza
Limpiar el texto del corpus con el fin de eliminar urls, stopword, números, entre otros.

### 4. Modelo y consulta
A partir del modelo generar los respectivos embeddings y realizar la ingesta a la base de datos vectorial (Chroma). Por último, buscador semántico construido en Gradio.
