# Predicción de Likes y Análisis de Tendencias de Videos

Este repositorio contiene el análisis y modelado de datos de videos de Youtube para Estados Unidos con el objetivo de **predecir la cantidad de likes** y estudiar los factores que influyen en la **velocidad de aparición en tendencias**.  

## Descripción del Proyecto

El estudio se centra en variables clave que afectan la interacción de los videos, incluyendo:

- **Categorías de contenido:** Music, Entertainment, Film & Animation, Howto & Style, Science & Technology, entre otras.
- **Métricas de interacción:** Número de vistas (*views*), comentarios (*comment_count*) y likes.
- **Fecha de publicación:** 
- **Sentimiento de los títulos:** Optimismo, decepción, desprecio, sumisión, entre otros.

### Hallazgos Principales

- Las categorías con **mayor interacción** son **Music**, **Entertainment** y **Film & Animation**, mientras que Entertainment concentra el **24.3 % de los videos**, seguido por Music (15.8 %) y Howto & Style (10.1 %).  
- El **número de vistas, comentarios, categoría y mes de publicación** son los factores más importantes para predecir los likes.  
- La **antigüedad del video** tiene un efecto negativo en la velocidad de tendencia (correlación = -0.7).  
- Las categorías con **menor tiempo para alcanzar la tendencia** son Science & Technology (0.67 días), Music (0.84 días) y Entertainment (0.95 días).  
- En cuanto al **sentimiento de los títulos**, los videos con títulos de sumisión se posicionan más rápido (8 días), seguidos de los neutrales (9 días) y los de desprecio (10 días).  

### Modelos de Predicción

Se evaluaron distintos enfoques de machine learning para predecir los likes:

- **Modelos basados en vecinos:** `KNeighborsRegressor`
- **Modelos basados en árboles de decisión:** `RandomForestRegressor`, `XGBRegressor`

Los modelos simples permiten capturar hasta un **87 % de la variabilidad** de los datos. La presencia de valores atípicos no afectó significativamente las métricas de rendimiento.  

### Requisitos

Para reproducir este proyecto se requiere **Python 3.12.11** y las siguientes librerías:

- `pandas` 2.3.0
- `numpy` 2.2.6
- `plotly` 6.2.0
- `urlextract` 1.9.0
- `emoji` 2.14.1
- `matplotlib` 3.10.3
- `seaborn` 0.13.2
- `scikit-learn` 1.7.0
- `xgboost` 3.0.4
- `optuna` 4.4.0
- `shap` 0.48.0
- `transformers` 4.52.4

Se recomienda crear un entorno virtual para instalar estas dependencias
 
