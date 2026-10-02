# Laboratorio 5 – Modelo espacial de cobertura hospitalaria

**Modelación y Simulación** · Estado de análisis: **Texas (EE.UU.)**

## Integrantes
- Humberto Alexander de la Cruz
- Daniel Oswaldo Juárez Herrera

## Objetivo
Construir un modelo espacial de cobertura hospitalaria para responder una pregunta de política pública: **¿qué fracción de la población de Texas tiene acceso a servicios hospitalarios dentro de una distancia razonable, y dónde están las brechas más críticas?**

Se usa Texas porque tiene 591 hospitales con datos de camas y 254 condados que mezclan grandes áreas metropolitanas con extensas zonas rurales.

## Datos (provistos en Canvas)
| Archivo | Contenido |
|---|---|
| `hospitales_eeuu.geojson` | 7,154 hospitales con camas totales, camas UCI y ocupación |
| `condados_eeuu.geojson` | 3,221 condados con geometría y código FIPS |
| `poblacion_condados.csv` | Población estimada por condado |
| `estados_eeuu.geojson` | Límites de los 51 estados |

## Alcance de esta entrega
- **Task 1:** carga y limpieza de datos, reproyección (EPSG:3083), estadísticas por condado y cobertura con buffers de 10, 25 y 50 km.
- **Task 2:** distancia al hospital más cercano, curva de cobertura acumulada, índice de vulnerabilidad por condado y selección de 3 nuevos hospitales con un algoritmo voraz para MCLP.

## Contenido
- `lab5.ipynb`: notebook con todo el análisis, ya ejecutado y comentado.
- `figures/`: mapas y gráficas generados por el notebook.
- `laboratorio_5.md`: enunciado.

## Cómo reproducirlo
1. Instalar dependencias:
   ```
   pip install geopandas pandas numpy matplotlib shapely scipy pyproj pyogrio matplotlib-scalebar jupyter
   ```
2. Colocar los cuatro archivos de datos en la raíz del proyecto.
3. Abrir `lab5.ipynb` y ejecutar todas las celdas. Las figuras se guardan en `figures/`.
