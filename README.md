<!-- =========================
     HERO
========================= -->

<p align="center">
  <img
    src="https://github.com/user-attachments/assets/9d748859-5c35-486e-bcb3-a0dc598d3905"
    alt="Kiva logo — Microloan Insights Dashboard"
    width="180"
  >
</p>

<h1 align="center">Kiva Microloan Insights (2025)</h1>

<p align="center">
  <strong>Dashboard interactivo en Excel</strong> · Exploración por <strong>sector</strong>, <strong>país</strong> y <strong>año</strong>
</p>

<p align="center">
  <a href="#tech-stack">Tech stack</a> ·
  <a href="#objetivo-analitico">Objetivo analítico</a> ·
  <a href="#sobre-el-proyecto">Sobre el proyecto</a> ·
  <a href="#limpieza-y-preparacion-del-dataset">Limpieza</a> ·
  <a href="#correccion-del-problema-del-slicer-country-vacio">Slicer</a> ·
  <a href="#que-incluye-el-dashboard">Dashboard</a> ·
  <a href="#diseno-y-accesibilidad">Diseño</a> ·
  <a href="#archivos-incluidos">Archivos</a> ·
  <a href="#fuente-de-datos">Fuente</a> ·
  <a href="#aprendizajes-clave">Aprendizajes</a>
</p>

<hr>

## Tech stack

- Excel  
- Power Query  
- Pivot Tables  
- Pivot Charts  
- Dashboard design  

<hr>

<p>
Desde siempre he estado muy vinculada a proyectos con impacto social. Mi experiencia en Health & Social Care me enseñó a mirar a las personas antes que a los números, y quizá por eso este proyecto me tocó de una forma especial.<br>
Trabajar con los datos de Kiva ha sido una forma de recordar por qué estoy aprendiendo análisis: porque los datos también pueden cambiar vidas cuando se leen con cuidado.
</p>

<hr>

## Objetivo analítico

Analizar la distribución de micropréstamos de Kiva para identificar patrones de financiación por sector, país y año, y construir un dashboard interactivo orientado a exploración y toma de decisiones.

<hr>

## Sobre el proyecto

Este trabajo explora más de <strong>42.000 micropréstamos de Kiva</strong>, con el objetivo de entender cómo se distribuye la financiación por <strong>sector</strong>, <strong>país</strong> y <strong>año</strong>, y qué patrones emergen cuando se observa con calma quién está recibiendo apoyo y para qué.

El resultado final es un <strong>dashboard interactivo en Excel</strong>, construido completamente desde cero con:

- PivotTables  
- PivotCharts  
- Slicers  
- Un tema de colores propio, inspirado en la identidad visual de Kiva  

Quise que no fuese “otro dashboard más”, sino una herramienta <strong>clara, accesible y agradecida de leer</strong>, incluso para quienes no tienen experiencia técnica.

<hr>

## Limpieza y preparación del dataset

El archivo original requería una preparación cuidadosa. Durante la limpieza:

- Organicé y normalicé las fechas; creé las columnas <code>loan_year</code> y <code>loan_month</code>.  
- Añadí <code>funding_gap</code> y <code>fully_funded</code>, esenciales para los KPIs del dashboard.  
- Reorganicé todas las columnas siguiendo un orden lógico: financieras → descriptivas → geográficas → temporales.  
  La columna <code>use</code> —muy extensa— quedó al final para no interrumpir la lectura del dataset.  
- Revisé valores incorrectos, inconsistencias y pequeños errores habituales en un CSV grande.  
- Detecté un registro con <strong>country vacío</strong>, que fue eliminado más adelante mediante <strong>Power Query</strong>.  

Cada paso me ayudó a comprender mejor la historia que había detrás de los datos, y no solo a dejarlos “limpios”.

<hr>

## Corrección del problema del slicer (country vacío)

Durante la revisión final del dashboard apareció un hueco en el slicer de <strong>country</strong>.  
La causa era un valor vacío heredado de versiones anteriores del dataset.

Para corregirlo:

1. Abrí el archivo en <strong>Power Query</strong>.  
2. Apliqué un filtro para eliminar filas sin valor en <code>country</code>.  
3. Guardé y actualicé todas las conexiones.  
4. Refresqué las PivotTables y sus slicers para sincronizar los cambios.  

El dashboard quedó completamente consistente y sin valores vacíos.

<hr>

## Qué incluye el dashboard

Una vez el dataset estuvo preparado, construí un dashboard que reúne:

### Visualizaciones principales

- <strong>Total Loan Amount by Sector</strong><br>
  Muestra dónde se concentran las necesidades económicas.

- <strong>Total Funded Amount by Sector (Completed Loans Only)</strong><br>
  Permite ver si la financiación acompaña esas necesidades.

- <strong>Top 10 Countries by Microloan Funding</strong><br>
  Una lectura rápida de dónde se moviliza mayor apoyo.

### KPIs

- <strong>Funding Rate: 100%</strong><br>
  Todos los préstamos del dataset aparecen como totalmente financiados.

- <strong>Top Funded Country: Philippines — 3.46M</strong>

- <strong>Top 10 Countries — Total Funding: 17.3M</strong>

### Slicers interactivos

- Sector  
- Country  
- Loan Year  

Todo sincronizado para facilitar la exploración.

<hr>

## Diseño y accesibilidad

Busqué que el dashboard fuera funcional, pero también amable de leer:

- Creé un <strong>tema personalizado</strong> basado en los tonos verdes de Kiva.  
- Incorporé el logotipo, el eslogan <em>“Loans That Change Lives”</em> y un enlace directo a <strong>About Us | Kiva</strong>.  
- Priorizo contrastes altos, tipografías claras y una estructura visual coherente.  
- Reduje la carga cognitiva: títulos directos, gráficos sencillos y etiquetas legibles.  


<hr>

## Archivos incluidos

- <strong>kiva_limpieza_v1.xlsx</strong> — dataset limpio y preparado  
- <strong>Kiva_Microloan_Insights_2025.xlsx</strong> — dashboard final  

<hr>

## Fuente de datos

El dataset original procede de Kaggle:

<strong>Data Science for Good — Kiva Crowdfunding</strong>  
https://www.kaggle.com/datasets/kiva/data-science-for-good-kiva-crowdfunding

No se incluye el dataset bruto completo en este repositorio por su tamaño.  
El archivo Excel incluido contiene la versión trabajada y preparada para análisis y dashboard.

### Reproducibilidad

Para reproducir el análisis desde cero, puede descargarse el dataset original desde Kaggle y aplicar los pasos de limpieza descritos en este README y en el archivo de preparación.

<hr>

### Nota sobre accesibilidad del README

Este documento sigue criterios de accesibilidad:

- estructura clara y jerárquica  
- párrafos cortos  
- lenguaje directo  
- listas bien delimitadas  
- ausencia de elementos decorativos innecesarios  
- contenido compatible con lectores de pantalla  

<hr>

## Aprendizajes clave

- Preparación y limpieza de datasets grandes en Excel  
- Uso de Power Query para transformación reproducible  
- Diseño de dashboards con criterios de claridad y accesibilidad  
- Uso de KPIs y segmentadores para exploración interactiva  

<hr>

