# 🏥 Accesibilidad a Hospitales y Clínicas en Lima Metropolitana

**Proyecto Final — Curso C2: Experto en Análisis Espacial en la Nube con Python**  
Centro de Altos Estudios en Geomática (CAEG)

---

## 📋 Descripción

Este proyecto evalúa la **accesibilidad espacial a establecimientos de salud** (hospitales y clínicas) en Lima Metropolitana, identificando zonas con déficit de cobertura mediante técnicas de análisis espacial en Python.

El análisis integra datos oficiales del MINSA, datos de OpenStreetMap y capas de densidad poblacional ráster (WorldPop) para responder: **¿qué zonas de Lima tienen acceso limitado a servicios de salud y cuántas personas viven en ellas?**

---

## 🗂️ Estructura del Repositorio

```
📁 proyecto-salud-lima/
├── 📓 Proyecto_Final_Lima_Hospitales.ipynb   # Notebook principal
├── 🌐 mapa_interactivo_salud_lima.html       # Mapa Folium exportado
├── 📊 dashboard_plotly_salud_lima.html       # Dashboard Plotly
├── 🗺️  mapa_plotly_salud_lima.html            # Mapa Plotly interactivo
├── 📁 outputs/
│   ├── mapa_distribucion_cobertura.png
│   ├── mapa_coropletico_distritos.png
│   ├── grafico_tipo_fuente.png
│   ├── grafico_distancias_accesibilidad.png
│   ├── grafico_ranking_distritos.png
│   ├── comparativo_servicios_urbanos.png
│   └── analisis_raster_poblacion.png
└── 📄 README.md
```

---

## 🚀 Cómo ejecutar

### Opción 1: Google Colab (recomendado)

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/alejandrovillaen-GIS/accesibilidad-salud-lima/blob/main/Proyecto_Final_Lima_Hospitales.ipynb)

1. Ir a [colab.research.google.com](https://colab.research.google.com)
2. **Archivo → Subir notebook** → seleccionar `Proyecto_Final_Lima_Hospitales.ipynb`
3. **Entorno de ejecución → Ejecutar todo** (`Ctrl + F9`)

> La primera celda instala todas las dependencias automáticamente.

### Opción 2: Local

```bash
git clone https://github.com/TU_USUARIO/proyecto-salud-lima.git
cd proyecto-salud-lima
pip install -r requirements.txt
jupyter notebook Proyecto_Final_Lima_Hospitales.ipynb
```

---

## 📦 Dependencias

```
geopandas>=0.14
pandas>=2.0
matplotlib>=3.7
seaborn>=0.12
folium>=0.14
contextily>=1.3
shapely>=2.0
requests>=2.28
rasterio>=1.3
rasterstats>=0.19
plotly>=5.15
mapclassify>=2.5
numpy>=1.24
```

---

## 📊 Fases del Proyecto

| Fase | Descripción | Módulos | Peso |
|------|-------------|---------|------|
| 1 | Preparación de datos | I, II, III, IV | 10% |
| 2 | Adquisición con Overpass API | VII | 15% |
| 3 | Análisis espacial (buffers, spatial joins, overlay) | V, VI | 25% |
| 4 | Visualización (Matplotlib, Seaborn, Folium) | IV, V | 20% |
| 5 | Interpretación y conclusiones | Transversal | 15% |
| ⭐ B1 | Automatización múltiples servicios con loops | III | +3% |
| ⭐ B2 | Dashboard interactivo con Plotly | IV | +2% |
| ⭐ B3 | Análisis ráster con Rasterio + estadísticas zonales | VI | +3% |
| ⭐ B4 | README y repositorio GitHub documentado | — | +2% |

---

## 🗺️ Fuentes de Datos

| Dataset | Fuente | Tipo | Licencia |
|---------|--------|------|----------|
| Establecimientos de salud Perú | MINSA / datos.gob.pe | CSV | CC BY |
| Hospitales y clínicas OSM | OpenStreetMap (Overpass API) | GeoJSON | ODbL |
| Límites distritales Lima | INEI / GeoBoundaries | GeoJSON | CC BY |
| Densidad poblacional | WorldPop 2020 (1 km) | GeoTIFF | CC BY |

---

## 🔍 Principales Hallazgos

- **Concentración de servicios** en Lima Moderna (San Isidro, Miraflores, Surco), contrastando con los conos Norte y Sur.
- **Distritos periurbanos** como Carabayllo, Puente Piedra y Villa María del Triunfo presentan los mayores déficits de cobertura.
- El análisis ráster estima que una fracción significativa de la población limeña vive a más de 1 km de cualquier hospital o clínica de nivel II/III.
- La automatización por loops permite replicar el análisis para farmaccias, colegios y comisarías con una sola llamada de función.

---

## 🛠️ Tecnologías utilizadas

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![GeoPandas](https://img.shields.io/badge/GeoPandas-0.14-green)
![Folium](https://img.shields.io/badge/Folium-0.14-darkgreen)
![Plotly](https://img.shields.io/badge/Plotly-5.15-purple)
![Rasterio](https://img.shields.io/badge/Rasterio-1.3-orange)

---

## 👤 Autor

**Alejandro Villavicencio Enciso**  
Geógrafo  
Curso C2 — CAEG  
Fecha de entrega: 15/04/2026  
GitHub: [@alejandrovillaen-GIS](https://github.com/alejandrovillaen-GIS)  
capacitaciones@caeg.pe | www.caeg.pe
