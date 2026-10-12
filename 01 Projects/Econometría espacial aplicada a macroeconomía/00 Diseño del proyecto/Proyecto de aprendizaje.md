---
tipo: proyecto
estado: activo
fecha_inicio: "2026-10-10"
fecha_limite: ""
area: "[[02 Áreas/Doctorado en geoinformática]]"
responsable: ""
tags:
  - econometria-espacial
  - macroeconomia
  - aprendizaje
---
# Econometría espacial aplicada a macroeconomía

## Propósito
Aprender desde fundamentos hasta métodos avanzados de econometría espacial, aplicándolos a preguntas macroeconómicas regionales de México. El resultado será un análisis reproducible, defendible y comunicable; no solo una colección de mapas o modelos.

## Pregunta paraguas
¿Cómo interactúan las economías regionales mexicanas en sus trayectorias de crecimiento y qué papel tienen la geografía, las redes productivas y los shocks comunes o localizados?

## Recomendación de tema central
**Convergencia y derrames del crecimiento económico entre entidades federativas mexicanas, 2003–último año comparable.** Es el punto de entrada más didáctico: permite construir una serie macroeconómica regional, medir desigualdad/convergencia, visualizar dependencia espacial y luego avanzar a paneles espaciales. El periodo final se fijará tras comprobar la continuidad y comparabilidad de las series.

### Pregunta de investigación inicial
¿Existe convergencia o divergencia del PIB real per cápita entre las entidades federativas, y cambian los resultados al modelar interdependencia espacial?

### Pregunta de extensión de frontera
¿Los shocks climáticos, las conexiones de cadenas productivas o la infraestructura digital alteran el crecimiento regional y producen efectos indirectos en regiones conectadas?

### Hipótesis de trabajo (se deben contrastar, no presuponer)
- La dependencia espacial cambia la estimación de la convergencia respecto de un modelo no espacial.
- La dirección/magnitud de los patrones depende de cómo se defina la interacción regional.
- Los efectos pueden ser heterogéneos por estructura productiva y posición en redes.

## Temas posibles
| Prioridad | Tema y pregunta | Valor para el perfil | Métodos por etapas | Viabilidad |
|---|---|---|---|---|
| 1 | **Convergencia del PIB real per cápita estatal.** ¿Las entidades rezagadas crecen más rápido? ¿Qué cambia al incluir interdependencia? | Economía macro + análisis espacial | Descripción, sigma/beta convergencia, Moran/LISA; SAR/SDM; panel FE | Alta con datos estatales comparables |
| 2 | **Shocks climáticos y convergencia regional.** ¿Temperatura, sequías y lluvia extrema modifican crecimiento y brechas, incluso en regiones vecinas? | Integra geoinformática, macro y clima | Panel descriptivo; clima no lineal; SDM dinámico; identificación cuasi-experimental avanzada | Media; alinear clima, unidad y output |
| 3 | **Cadenas productivas y nearshoring.** ¿La articulación interregional difunde productividad/empleo o concentra beneficios? | Economía aplicada y emprendimiento | Red insumo-producto, concentración, Gini espacial; modelos de panel con pesos económicos | Media; requiere matriz interregional y proxies consistentes |
| 4 | **Infraestructura digital y productividad regional.** ¿El acceso a banda ancha/digitalización se asocia a crecimiento local y efectos en zonas conectadas? | Geoinformática y emprendimiento | Mapeo, clusters, panel espacial; luego despliegue cuasi-experimental si se sostiene | Media-baja; la cobertura y medición son retos |
| 5 | **Gasto público y derrames fiscales.** ¿La inversión local impulsa actividad propia o de territorios conectados? | Política macroeconómica | Descriptivos; panel espacial; VAR espacial; diseño causal posterior | Media |
| 6 | **Pobreza y trampas espaciales.** ¿Persisten clusters o clubes de movilidad entre municipios? | Desarrollo regional y política pública | Mapas, Moran/LISA, transiciones espaciales, convergencia distributiva | Media; municipal y pocos años comparables |
| 7 | **Transición energética y brechas urbano-rurales.** ¿La inversión renovable se vincula con empleo/actividad y con qué heterogeneidad territorial? | Geoinformática + sostenibilidad | GIS, panel espacial, no linealidad y heterogeneidad | Media-baja; geodatos de proyectos y series |
| 8 | **Transmisión espacial de precios o shocks macroeconómicos.** ¿Cómo se difunden cambios de precios/actividad entre ciudades por rutas y mercados? | Macroeconomía aplicada | Series regionales, redes, GVAR/SpVAR, respuestas impulso | Baja como primer proyecto; avanzado |

## Ruta desde nivel básico hasta especializado
1. **Base estadística y geográfica:** descriptiva, álgebra matricial esencial, regresión OLS, lectura de mapas, polígonos, claves geoestadísticas, proyecciones/CRS, datos panel.
2. **Exploración espacial:** hipótesis para vecindad, matrices W, Moran global y LISA; aprender que autocorrelación describe patrones, no demuestra causalidad.
3. **Regresión espacial transversal:** OLS y diagnóstico; SAR/SLM, SEM, SLX, SDM; comparación de especificaciones y efectos directos, indirectos y totales.
4. **Panel macro regional:** efectos fijos de unidad y tiempo, panel espacial estático y dinámico; dependencia transversal y shocks comunes.
5. **Interacciones económicas:** comparar W de contigüidad/distancia con redes de comercio, movilidad o insumo-producto; justificar el mecanismo y probar sensibilidad.
6. **Frontera metodológica:** heterogeneidad espacial, no linealidades, GVAR/SpVAR o métodos bayesianos según la pregunta; ML espacial para predicción/heterogeneidad y validación espacial por bloques.
7. **Inferencia causal espacial:** solo cuando exista tratamiento/exposición, contrafactual y supuestos defendibles; definir exposición de vecinos/interferencia, DiD/IV/event study y robustez. Un SDM por sí solo no convierte asociación en causalidad.

## Entregables del proyecto
- [ ] Protocolo de investigación con pregunta, mecanismo, unidad, periodo y criterios de éxito.
- [ ] Ficha de datos y diccionario de variables.
- [ ] Cuaderno/script reproducible y registro de versiones.
- [ ] Diagnóstico descriptivo y mapas de referencia.
- [ ] Justificación teórica de W y sensibilidad a matrices alternativas.
- [ ] Estimaciones base y modelo espacial con interpretación de impactos.
- [ ] Sección de limitaciones, incertidumbre y alcance causal.
- [ ] Presentación académica visual/animada y exposición oral.

## Siguiente acción
- [ ] Descargar y revisar cobertura/metadatos del PIB estatal y población, definir si la unidad inicial será entidad federativa, y fijar el periodo común.

## Criterios de rigor
- Distinguir correlación espacial, spillover estimado e identificación causal.
- Hacer explícita la unidad espacial modificable (MAUP), pesos W, fronteras y cobertura temporal.
- Reportar datos faltantes, cambios metodológicos y sensibilidad.
- No comparar PIB nominal como si midiera crecimiento real.
- Informar impactos marginales y su incertidumbre; no interpretar solamente el signo de los coeficientes SDM.
- Usar CV espacial/bloques cuando el objetivo sea predicción, en lugar de partición aleatoria que filtre información vecina.

## Equipo de asesoría
Se desplegaron **tres subagentes**, de acuerdo con el número solicitado: (1) investigación y revisión temática; (2) métodos/modelos espaciales; (3) economía y estadística descriptiva. La perspectiva de presentaciones académicas animadas se integra en [[../03 Presentación académica/Guion para presentación académica animada]].
