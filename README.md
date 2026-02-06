# Clasificación de la longevidad en la NBA

## Descripción
Este proyecto estudia la longevidad de los jugadores de la NBA mediante técnicas de clasificación supervisada. La longevidad se define como la permanencia de un jugador en la liga durante más de cinco temporadas. El objetivo principal es identificar qué características de rendimiento, participación y eficiencia están asociadas a carreras profesionales más largas.

## Dataset
Se utiliza el dataset **NBA Players Data (1996–2021)** obtenido de Kaggle, que contiene información a nivel de temporada sobre jugadores de la NBA, incluyendo métricas de rendimiento ofensivo, eficiencia y participación en el juego.

## Procesado y análisis inicial
- Limpieza de datos y tratamiento de variables inconsistentes.
- Construcción de la variable objetivo `career_5plus`.
- Análisis exploratorio y comparación de variables entre clases.
- Estudio de correlaciones para detectar redundancias.
- Aplicación de PCA para comprender la estructura de las variables.
- Análisis ANOVA para identificar variables con diferencias significativas entre clases.

## Modelos de clasificación
Se implementaron y compararon los siguientes algoritmos:
- Regresión logística (baseline)
- K-Nearest Neighbors (KNN) con optimización mediante Grid Search
- Árbol de decisión regularizado
- Support Vector Machine (SVM) con kernel RBF

Los modelos se evaluaron utilizando métricas como accuracy, matriz de confusión, precision, recall y F1-score, prestando especial atención a la detección de jugadores con carreras largas.

## Resultados principales
Los modelos no lineales superan claramente al baseline logístico, confirmando que la longevidad en la NBA no responde a relaciones lineales simples. El árbol de decisión regularizado ofrece el mejor equilibrio entre rendimiento predictivo e interpretabilidad, permitiendo extraer reglas claras sobre los factores que influyen en la duración de la carrera profesional.

## Insight clave
La longevidad en la NBA está más asociada a la capacidad de mantener una participación constante y aportar valor de forma eficiente dentro de un rol claro que a características físicas o expectativas iniciales como el puesto de draft.

## Tecnologías utilizadas
- Python
- pandas, numpy, scipy
- scikit-learn
- matplotlib / seaborn

## Autor
Proyecto realizado como parte de la asignatura **MD005 – Sistemas Basados en el Conocimiento**.
