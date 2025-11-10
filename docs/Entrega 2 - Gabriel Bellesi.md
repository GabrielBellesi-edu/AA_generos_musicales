# Entrega 2: Acceso y Descripción del Dataset

## 1. Origen del dataset

En este proyecto se aplicarán técnicas de **Aprendizaje Supervisado** con el objetivo de desarrollar un modelo capaz de **clasificar el género musical de una canción** a partir de sus características de audio y metadatos obtenidos de **Spotify**.

Originalmente el dataset utilizado provenía de **Kaggle**, bajo el título *“Spotify Data Visualization”*, y contenía **2000 registros de canciones populares** comprendidas entre los años **2000 y 2019**.

Sin embargo, por recomendación del profesor, quien sugirió trabajar con un conjunto de datos más actualizado, se intentó buscar un nuevo dataset de Spotify que incluyera las características de audio más recientes.  
Durante la investigación se comprobó que la **API de Spotify ya no ofrece acceso directo** a dichas variables, por lo que fue necesario recurrir a otras fuentes.

La solución adoptada consistió en **construir un dataset propio**, recopilando canciones desde servicios como **Spotify** y **YouTube Music**, y complementando sus características de audio mediante la herramienta **Reccobeats**.  

No obstante, debido a que Reccobeats no es un servicio ampliamente utilizado, **no todas las canciones disponen de las características acústicas completas** necesarias para desarrollar el modelo de aprendizaje automático.  
Por esta razón, el dataset final **comprende aproximadamente 743 canciones**, distribuidas en **11 géneros musicales**.

---

## 2. Descripción general del dataset

El dataset final combina información obtenida manualmente de playlists musicales y los valores acústicos proporcionados por Reccobeats.  
Cada registro representa una canción individual y contiene información tanto **categórica** (como el artista o el género) como **numérica** (como la energía o el tempo).

- **Cantidad de instancias originales:** 2564 canciones  
- **Cantidad de instancias finales:** 743 canciones  
- **Cantidad de características (columnas):** 20  
- **Tipos de datos:** string, integer, float  
- **Variable objetivo:** `genero`

---

## 3. Estructura del dataset

| Campo              | Tipo     | Descripción |
|--------------------|----------|-------------|
| **id**             | string   | Identificador único de la pista. |
| **href**           | string   | Enlace directo a la canción en Spotify. |
| **spotify_id**     | string   | ID de Spotify para la pista. |
| **artista**        | string   | Nombre del artista que interpreta la canción. |
| **tema**           | string   | Nombre de la canción. |
| **genero**         | string   | Género musical, derivado de la playlist de origen. |
| **fuente**         | string   | Servicio desde el cual proviene la playlist. |
| **año**            | integer  | Año de lanzamiento de la canción. |
| **popularidad**    | integer  | Popularidad de la pista (0 a 100), calculada por algoritmo según reproducciones y actualidad. |
| **acousticness**   | float    | Nivel de acústica (0.0–1.0), indica cuán orgánica es la canción. |
| **danceability**   | float    | Bailabilidad (0.0–1.0), mide cuán apta es la canción para bailar. |
| **energy**         | float    | Energía (0.0–1.0), refleja intensidad y vitalidad. |
| **instrumentalness** | float  | Probabilidad de que la pista sea instrumental (0.0–1.0). |
| **key**            | integer  | Tono musical (0=C, 1=C♯/D♭, etc.). |
| **liveness**       | float    | Presencia en vivo; valores > 0.8 indican grabaciones con audiencia. |
| **loudness**       | float    | Volumen promedio en decibelios (dB). |
| **mode**           | integer  | Modalidad: 1 = mayor, 0 = menor. |
| **speechiness**    | float    | Nivel de habla (0.0–1.0), mide presencia de palabras habladas. |
| **tempo**          | float    | Tempo estimado en beats por minuto (BPM). |
| **valence**        | float    | Valencia emocional (0.0–1.0), mide el tono emocional: triste ↔ alegre. |

---

## 4. Características generales y preprocesamiento

Durante la construcción y limpieza del dataset se realizaron las siguientes acciones:

- **Eliminación de duplicados**: se removieron canciones repetidas provenientes de distintas playlists.  
- **Normalización de nombres de columnas y artistas** para garantizar consistencia.  
- **Conversión de tipos de datos**:  
  - Variables numéricas (`float`, `integer`) fueron convertidas para su posterior normalización.  
  - Variables categóricas (`artista`, `genero`, `fuente`) se mantuvieron en formato `string`.  
- **Verificación de valores faltantes**: las canciones sin valores acústicos completos fueron excluidas.  

El dataset final está almacenado en el repositorio en la carpeta:

```

data/processed/04_dataset_filtrado.csv

```

---

## 5. Observaciones finales

Este dataset constituye la base sobre la cual se entrenarán los modelos de **clasificación supervisada**.  
Su estructura y contenido permiten explorar la relación entre **características acústicas** y **género musical**, así como comparar el desempeño de distintos algoritmos de aprendizaje automático (KNN, Árbol de Decisión, Random Forest, SVM, entre otros).

---

**Fecha de adquisición:** Octubre–Noviembre 2025  
**Fuentes de datos:** Spotify, YouTube Music, Reccobeats  
**Cantidad final de registros:** 743 canciones  
**Cantidad de géneros representados:** 11  

---

**Archivo del dataset:** `04_dataset_filtrado.csv`  
**Ubicación en el repositorio:** `data/processed/`  
```

---
