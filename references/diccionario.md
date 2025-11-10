Claro, Gabriel. Aquí tenés el contenido formateado en Markdown con las explicaciones traducidas al español:

---

## 🎵 Atributos de Pistas

| Campo            | Tipo     | Descripción en Español |
|------------------|----------|-------------------------|
| **id**           | string   | Identificador único de la pista. |
| **href**         | string   | Enlace directo a la canción en Spotify. |
| **spotify_id**   | string   | ID de Spotify para la pista. |
| **artista**      | string   | Nombre del artista que interpreta la canción. |
| **tema**         | string   | Nombre de la canción. |
| **genero**       | string   | Género musical, derivado de la playlist de origen. |
| **fuente**       | string   | Servicio desde el cual proviene la playlist. |
| **año**          | integer  | Año de lanzamiento de la canción. |
| **popularidad**  | integer  | Popularidad de la pista, valor entre 0 y 100. Calculado por algoritmo según la cantidad total de reproducciones y su actualidad. Las canciones reproducidas recientemente tienen mayor puntuación. Las versiones duplicadas (por ejemplo, de un álbum y un single) se califican por separado. La popularidad del artista y del álbum se deriva matemáticamente de la popularidad de sus pistas. Este valor puede tener un pequeño retraso respecto a la popularidad real, ya que no se actualiza en tiempo real. |
| **acousticness** | float    | Acústica: mide cuánto de la canción está compuesto por sonidos naturales u orgánicos. Va de 0.0 a 1.0, donde valores más altos indican mayor probabilidad de que la pista sea acústica. |
| **danceability** | float    | Bailabilidad: indica cuán adecuada es la canción para bailar, considerando ritmo, consistencia del beat, tempo y energía. Va de 0 (nada bailable) a 1 (muy bailable). |
| **energy**       | float    | Energía: mide la intensidad y vitalidad de una pista. Un valor de 0 representa una canción tranquila o relajada, mientras que 1 indica una pista intensa y enérgica. |
| **instrumentalness** | float | Instrumentalidad: estima la probabilidad de que una pista no tenga voces. Valores cercanos a 1.0 indican mayor probabilidad de ser instrumental. |
| **key**          | integer  | Tono musical de la pista, usando notación de clase de tono: 0 = C, 1 = C♯/D♭, 2 = D, etc. Si no se detecta tono, el valor es -1. |
| **liveness**     | float    | Presencia en vivo: detecta si hay audiencia en la grabación. Valores mayores a 0.8 sugieren que la pista fue grabada en vivo. |
| **loudness**     | float    | Volumen general de la pista en decibelios (dB), promediado a lo largo de toda la canción. Valores típicos van de -60 a 0 dB. |
| **mode**         | integer  | Modalidad: indica si la pista está en modo mayor (1) o menor (0). |
| **speechiness**  | float    | Nivel de habla: detecta la presencia de palabras habladas. Valores cercanos a 1.0 indican grabaciones predominantemente habladas. Entre 0.33 y 0.66 puede haber mezcla de música y habla. Por debajo de 0.33 es principalmente música. |
| **tempo**        | float    | Tempo estimado de la pista en beats por minuto (BPM). Valores típicos van de 0 a 250. |
| **valence**      | float    | Valencia emocional: mide el tono emocional de la pista. Un valor de 0 indica una canción triste o sombría, mientras que 1 representa una canción alegre o positiva. |

---
