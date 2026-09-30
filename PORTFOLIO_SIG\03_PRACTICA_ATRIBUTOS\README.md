# Práctica 3 — Análisis de atributos y estadísticas vectoriales

## Descripción

Análisis estadístico de la red vial provincial mediante el uso de atributos vectoriales en QGIS.

El objetivo fue analizar la distribución de los tramos de la red vial según el campo categórico `rst`, obteniendo la cantidad y el porcentaje correspondiente a cada categoría.

## Datos utilizados

* **Fuente:** Instituto Geográfico Nacional (IGN)
* **Capa:** Red vial provincial
* **Formato:** Shapefile
* **CRS:** EPSG:4326 — WGS 84
* **Campo analizado:** `rst`

## Metodología

1. Carga de la capa oficial de la red vial provincial.
2. Identificación del campo categórico `rst`.
3. Aplicación de la herramienta **Estadísticas por categorías** de QGIS.
4. Cálculo de la cantidad de tramos correspondientes a cada categoría.
5. Cálculo del porcentaje sobre el total de tramos.
6. Representación cartográfica mediante simbología categorizada.
7. Elaboración del mapa final con información técnica, fuente, escala, orientación y metadatos.

## Resultados

| Categoría RST | Cantidad de tramos | Porcentaje |
| ------------- | -----------------: | ---------: |
| RST 1         |              8.019 |    62,03 % |
| RST 2         |              2.430 |    18,80 % |
| RST 3         |              2.479 |    19,17 % |
| **Total**     |         **12.928** |  **100 %** |

## Productos

* `Mapa_Analisis_Atributos_RST.pdf` — mapa final en formato PDF.
* `Mapa_Analisis_Atributos_RST.png` — visualización del mapa.
* `Practica_03_Analisis_Atributos.qgz` — proyecto QGIS.
* `Estadisticas_rst.gpkg` — tabla de resultados estadísticos.

## Herramientas y competencias

* QGIS 3.44.13
* Análisis de atributos vectoriales
* Estadística por categorías
* Cálculo de porcentajes
* Simbología categorizada
* Cartografía temática
* Gestión de datos vectoriales
* Interpretación de resultados SIG

## Fuente

Instituto Geográfico Nacional (IGN) — Red vial provincial.

## Autor

**Héctor Acuña**

**Fecha:** 30/09/2026
