# Análisis de accesibilidad vial mediante PostgreSQL/PostGIS y QGIS

## Descripción

Proyecto SIG orientado al análisis de la accesibilidad vial alrededor de un punto de interés.

Se definió un área de influencia de **5 km alrededor de un Cerro** y se analizaron los tramos de la red vial provincial que se encuentran dentro o próximos a esta zona.

El objetivo fue aplicar herramientas de **PostGIS para análisis espacial**, integrando los resultados con **QGIS** para su visualización y representación cartográfica.

## Herramientas utilizadas

* PostgreSQL
* PostGIS
* QGIS
* SQL
* Sistema de coordenadas EPSG:32720 — WGS 84 / UTM zone 20S

## Datos utilizados

* Red vial provincial.
* Punto de referencia correspondiente al Cerro.
* Área de influencia de 5 km.

## Metodología

1. Carga de la red vial en PostgreSQL/PostGIS.
2. Definición del punto de referencia en EPSG:4326.
3. Transformación de los datos a EPSG:32720 para realizar cálculos métricos.
4. Generación de un buffer de 5 km.
5. Identificación de los tramos viales que intersectan el área de influencia.
6. Cálculo de la distancia entre los tramos viales y el Cerro.
7. Cálculo de la longitud de los tramos.
8. Clasificación de los tramos según su distancia al punto de referencia.
9. Cálculo de kilómetros de infraestructura vial dentro del área de influencia.
10. Integración de los resultados en QGIS y elaboración del mapa final.

## Funciones PostGIS utilizadas

* `ST_Transform`
* `ST_SetSRID`
* `ST_MakePoint`
* `ST_Buffer`
* `ST_DWithin`
* `ST_Distance`
* `ST_Intersects`
* `ST_Intersection`
* `ST_Length`

También se utilizaron operaciones SQL como:

* `COUNT`
* `SUM`
* `GROUP BY`
* `ORDER BY`
* `CASE`
* creación de vistas mediante `CREATE VIEW`

## Resultados

El análisis identificó:

* **4 tramos viales** dentro de un radio de 5 km.
* **60,95 km** de longitud total considerando los tramos completos.
* **16,42 km** de infraestructura vial ubicada dentro del área de influencia de 5 km.

### Distribución según distancia

| Rango de distancia | Cantidad de tramos |
| ------------------ | -----------------: |
| 0–1 km             |                  1 |
| 1–2 km             |                  3 |
| 2–3 km             |                  0 |
| 3–5 km             |                  0 |

## Producto cartográfico

Se elaboró un mapa final en QGIS incorporando:

* Red vial provincial.
* Área de influencia de 5 km.
* Punto de referencia.
* Tramos viales analizados.
* Clasificación por distancia.
* Escala gráfica.
* Orientación norte.
* Sistema de referencia.
* Fuente de datos.
* Autor y fecha.

## Competencias demostradas

Este proyecto demuestra conocimientos en:

* Análisis espacial con PostGIS.
* Consultas SQL sobre datos geográficos.
* Cálculos de distancia y longitud.
* Análisis mediante buffers.
* Intersección de geometrías.
* Agregación y clasificación de datos espaciales.
* Integración PostgreSQL/PostGIS con QGIS.
* Elaboración de cartografía temática.
* Organización de resultados para documentación técnica.
