---
tipo: mapa-metodologico
estado: lectura
fecha: "2026-10-10"
tags:
  - econometria-espacial
  - metodologia
---
# Métodos, exponentes y herramientas

## Referentes principales
- **Luc Anselin:** bases de econometría espacial, diagnóstico, Moran/LISA, modelos SAR/SEM y GeoDa/PySAL.
- **James LeSage y Robert Pace:** interpretación de impactos en modelos espaciales, multiplicadores y efectos directos/indirectos/totales.
- **J. Paul Elhorst:** panel espacial, modelos dinámicos y puente con macroeconomía regional.
- **Sergio J. Rey:** análisis espacial exploratorio, desigualdad/movilidad regional y ecosistema PySAL.
- **Kelejian y Prucha:** estimación instrumental/generalizada para modelos espaciales.
- **Reich, Cressie y colaboradores; Pollmann:** inferencia causal espacial y tratamientos con interferencia.

## Modelos en el mapa de aprendizaje
| Familia | Qué representa | Cuándo considerar |
|---|---|---|
| OLS + diagnóstico | Referencia no espacial | Siempre como línea base; inspeccionar residuos |
| SAR/SLM | Interacción/rezago de resultado Wy | Cuando el mecanismo implica interacción en resultados |
| SEM | Dependencia espacial del error | Dependencia no modelada por covariables/interacción explícita |
| SLX | Rezagos espaciales de X | Efectos de exposición/covariables vecinas |
| SDM | Wy y WX | Modelo flexible para efectos locales y spillovers de regresores |
| SAC/SARAR/GNS | Combinaciones de dependencia en resultado/error/X | Solo con teoría, identificación y diagnóstico que lo requieran |
| Panel espacial FE | Heterogeneidad fija y dependencia espacial | Datos repetidos por región y tiempo |
| Panel dinámico / SpVAR / GVAR | Propagación temporal y entre unidades | Preguntas sobre shocks macroeconómicos y respuestas dinámicas |
| Regímenes/coeficientes variables | Heterogeneidad territorial | Hipótesis explícitas sobre diferencias por región/sector |
| Bayes/INLA | Incertidumbre y estructura espacial latente | Problemas con jerarquía/escala; elección justificada |
| Causalidad espacial | Tratamientos y exposición a regiones vecinas | Solo con diseño causal/supuestos y contrafactual claros |
| ML espacial | Predicción/heterogeneidad | Complemento; CV espacial y no atribuir causalidad automática |

## Avance actual del área
La innovación no consiste simplemente en agregar un rezago espacial. La literatura reciente enfatiza (a) relacionar W con el mecanismo económico —fronteras, distancia, flujos o redes—; (b) separar efectos directos, indirectos y totales; (c) incorporar heterogeneidad, dinámica y factores comunes; y (d) resolver identificación cuando una política o shock afecta también unidades cercanas. El puente entre macroeconomía regional, modelos de panel espaciales y GVAR está creciendo. El artículo de revisión de *Spatial Macroeconomics* documenta la unión de macro, geografía económica, redes productivas y panel espacial; véase Bond-Smith et al. (2024) en Bibliografía.

## Herramientas recomendadas por fase
- **GeoDa:** primeras exploraciones, mapas de Moran/LISA y regresión espacial.
- **Python:** GeoPandas, libpysal, esda y spreg/PySAL para geoprocesamiento y modelos espaciales reproducibles.
- **R:** sf, spdep, spatialreg y splm; INLA para modelos latentes espaciales cuando proceda.
- **QGIS:** inspección y elaboración cartográfica.
- **PostGIS/SQL:** almacenamiento y consultas geoespaciales cuando el volumen crezca.
- **Stata:** panel espacial con comandos compatibles y matriz de pesos.

La selección final debe cotejar capacidades y versiones en documentación oficial vigente; esta lista no presupone que todas las rutinas estimen cualquier modelo dinámico o causal.

## Validaciones indispensables
- Mecanismo y fuente de W, escala/unidad y sensibilidad a alternativas plausibles.
- Diagnóstico y criterios de especificación; análisis de residuos y dependencia transversal.
- Coeficientes no equivalen directamente a impactos marginales en modelos con rezagos espaciales.
- Impactos y errores/incertidumbre; dependencia entre regiones y shocks comunes.
- Endogeneidad de Wy, WX o redes construidas a partir de resultados.
- MAUP, cambios geográficos/temporales, límites y errores de medición.
- Inferencia causal requiere diseño; regresión espacial no identifica causalidad automáticamente.
