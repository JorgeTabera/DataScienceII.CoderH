# 🎵 Proyecto: Análisis de Playlists de Spotify

## 📌 Abstracto y motivación
Este proyecto tiene como objetivo analizar las tendencias musicales en Argentina a partir de la playlist **Top 50 Argentina** de Spotify.  
La motivación es entender qué artistas, géneros y lanzamientos concentran mayor popularidad y cómo estos insights pueden ser útiles para **ejecutivos de la industria musical, curadores de playlists y equipos de marketing**.

---

## 🎯 Preguntas / Hipótesis
- ¿Qué artistas dominan el Top 50 actual?  
- ¿Qué géneros musicales son más frecuentes en la playlist?  
- ¿Qué proporción de artistas son locales vs internacionales?  
- ¿Qué canciones tienen mayor popularidad y por qué?  
- ¿Existe relación entre la popularidad del artista y la del track?  
- ¿Los lanzamientos recientes tienen mayor presencia en el ranking?  
- ¿Qué géneros están asociados a mayor popularidad?  

---

## 📂 Dataset y Metadata
- **Fuente:** API pública de Spotify  
- **Playlist analizada:** Top 50 Argentina  
- **Filas:** 50 tracks  
- **Columnas principales:**  
  - `puesto`, `nombre`, `artistas`, `Artista_Princ`, `album`  
  - `popularidad`, `release_date`, `genres`, `followers`, `artist_popularity`  
- **Variables clave:** popularidad del track, popularidad del artista, géneros, seguidores, año de lanzamiento  

---

## ⚙️ Metodología
1. **Extracción de datos** vía API de Spotify (tracks, artistas y álbumes).  
2. **Limpieza y transformación**: construcción de `df_tracks`, `df_artists`, `df_albums`.  
3. **Enriquecimiento**: merge en `df_final` con información de artistas y álbumes.  
4. **Exportación a CSV** para reproducibilidad (`final_latest.csv`).  
5. **EDA y visualizaciones** para responder las hipótesis.  

---

## 📊 Visualizaciones principales
- **Top artistas por presencia** → barplot horizontal.  
- **Géneros más frecuentes** → barplot.  
- **Locales vs internacionales** → gráfico circular.  
- **Canciones más populares** → barplot con top 10 tracks.  
- **Popularidad artista vs track** → scatterplot con correlación y casos outliers.  
- **Lanzamientos recientes** → histograma / barras por periodo.  
- **Popularidad por género** → boxplot/violin plot.  

---

## 🔎 Insights finales
- Los **géneros urbanos** (trap latino, reggaetón) dominan el Top 50.  
- Las **colaboraciones** potencian la popularidad de los tracks.  
- Los **lanzamientos recientes** concentran gran parte de la presencia en el ranking.  
- La **escena local** mantiene peso frente a artistas internacionales.  
- Existen casos donde el **track supera ampliamente la popularidad del artista**, reflejando fenómenos de viralidad.  

---

## 🚀 Próximos pasos
- Enriquecer el análisis con **audio features** (danceability, energy, valence).  
- Incorporar métricas de **engagement social**.  
- Extender el análisis a otras playlists y regiones.  

---

## 🔧 Reproducibilidad
- El notebook está diseñado para ejecutarse en **Google Colab** o **Jupyter Notebook**.  
- Los datos se guardan en CSV (`final_latest.csv`) para evitar re-llamar a la API en cada ejecución.  
- Las credenciales de Spotify deben mantenerse en un archivo seguro (`SpotCredDSII.txt` en Google Drive).  

---

## 📎 Repositorio
Este proyecto incluye:  
- Notebook (`Proyecto_Spotify_DS_II.ipynb`)  
- Presentación ejecutiva (PDF/Slides)  
- Archivos CSV exportados (`final_latest.csv`, `tracks_YYYYMMDD.csv`, etc.)  

---
