---
tipo: protocolo-datos
estado: por-iniciar
unidad: entidad-federativa
pais: Mexico
periodo: "2003–por definir"
fuentes: []
tags:
  - macroeconomia
  - datos-espaciales
---
# Plan de datos y análisis descriptivo

## Diseño recomendado para el primer laboratorio
Empezar con las 32 entidades federativas, PIB por entidad y población. Preferir una serie a precios constantes/volumen para estudiar crecimiento real; documentar la base, unidades, revisiones y año inicial/final. ITAEE sirve como indicador de coyuntura, pero no es PIB. No comenzar con PIB municipal anual si la variable no está publicada con la misma cobertura y metodología.

## Variables
- Resultado principal: PIB real per cápita, nivel y tasa de crecimiento anual.
- Complementarias: población, PIB sectorial, empleo/productividad aproximada si sus denominadores y cobertura son consistentes.
- Para extensiones: anomalías de temperatura/precipitación; inversión y empleo manufacturero; acceso digital; gasto público; pobreza en sus años disponibles.

## Flujo reproducible
1. Registrar fuente, fecha de descarga, identificador geográfico y licencia/uso.
2. Unificar claves estatales; verificar cambios de límites, faltantes y duplicados.
3. Homologar precios, unidades y población. Mantener columnas originales y transformadas.
4. Graficar series por entidad, distribución, crecimiento anual, cuantiles y mapas con una escala cromática fija.
5. Medir desigualdad interregional (desviación estándar de log PIB per cápita, CV o Theil), explicitar ponderación por población y calcular convergencia sigma.
6. Construir mapa de Moran, I de Moran global por año y LISA con permutaciones; reportar significancia y corrección por pruebas múltiples cuando corresponda.
7. Comparar W queen/rook, k vecinos y distancia solo si son coherentes con la hipótesis. Para temas productivos, comparar en fase avanzada contra matriz económica/red.
8. Guardar tabla procesada, límites utilizados, código, entorno, semilla y registro de decisiones.

## Lectura descriptiva correcta
Moran global pregunta si valores similares tienden a agruparse bajo W. LISA localiza clusters/outliers relativos a esa misma W. Un cluster de crecimiento o un Moran significativo no permite afirmar que una entidad cause el crecimiento de otra.

## Datos mexicanos candidatos
- INEGI, PIB por entidad federativa: https://www.inegi.org.mx/temas/pibent/
- INEGI, ITAEE (indicador trimestral; útil como extensión de coyuntura, no sustituye PIB): https://www.inegi.org.mx/programas/itaee/
- INEGI, Censo de Población y Vivienda 2020: https://www.inegi.org.mx/programas/ccpv/2020/
- CONEVAL, pobreza municipal 2010, 2015 y 2020: https://www.coneval.org.mx/Medicion/Paginas/Pobreza-municipio-2010-2020.aspx
- OECD Regional Statistics, para comparación internacional y definiciones regionales: https://data-explorer.oecd.org/

Estos son portales estadísticos institucionales para obtener datos primarios; la fundamentación de métodos e interpretación se documenta en la bibliografía académica del proyecto.
