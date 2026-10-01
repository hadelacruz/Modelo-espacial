# Laboratorio 5 – Modelo espacial de cobertura de servicios de salud

**Modelación y Simulación** · Territorio de análisis: **Guatemala**

## Integrantes
- Humberto Alexander de la Cruz
- Daniel Oswaldo Juárez Herrera

## Objetivo
Construir un modelo espacial con datos geoespaciales públicos para responder una pregunta de política pública: **¿qué fracción de la población de Guatemala tiene acceso a servicios de salud dentro de una distancia razonable, y dónde están las brechas más críticas?**

Para ello se combinan tres fuentes de datos descargadas desde Python:

| Dato | Fuente |
|---|---|
| Divisiones administrativas (22 departamentos, 354 municipios) | [GADM 4.1](https://gadm.org/) |
| Instalaciones de salud | [Global Healthsites Mapping Project](https://healthsites.io/) (API v3) |
| Densidad poblacional 2020, 1 km | [WorldPop](https://www.worldpop.org/) |

## Alcance de esta entrega
- **Task 1:** descarga de datos, análisis exploratorio, buffers de cobertura de 5, 10 y 20 km y población cubierta.
- **Task 2:** sensibilidad de la cobertura (curva de 1 a 50 km), índice compuesto de vulnerabilidad por municipio y ubicación de 5 nuevas instalaciones con un algoritmo voraz para MCLP.

## Contenido
- `lab5.ipynb`: notebook con todo el análisis, comentado.
- `build_notebook.py`: script que genera el notebook.
- `laboratorio_5.md`: enunciado.

## Cómo reproducirlo
1. Instalar dependencias:
   ```
   pip install geopandas pandas numpy matplotlib requests shapely rasterio scipy pyproj pyogrio matplotlib-scalebar python-dotenv jupyter
   ```
2. Crear un archivo `.env` en la raíz con la llave de Healthsites (debe estar aprobada por sus administradores):
   ```
   HEALTHSITES_API_KEY=su_llave
   ```
3. Abrir `lab5.ipynb` y ejecutar todas las celdas. Los datos se descargan solos en `data/` y las figuras se guardan en `figures/`.

> `.env` y `data/` están en `.gitignore` y no se suben al repositorio.
