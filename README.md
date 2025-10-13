
---

# **Impacto de la electrificación del transporte en las emisiones de GEI en Europa**

[![GitHub last commit](https://img.shields.io/github/last-commit/LoFloAb/Impacto_de_la_electrificaci-n_del_transporte_en_las_emisiones_de_GEI_en_Europa?style=plastic&color=brightgreen)](https://github.com/LoFloAb/Impacto_de_la_electrificaci-n_del_transporte_en_las_emisiones_de_GEI_en_Europa)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=plastic)](https://opensource.org/licenses/MIT)

Este proyecto analiza la evolución de las emisiones de gases de efecto invernadero (GEI) en Europa, los cambios en la matriculación de nuevos vehículos y la evolución del parque automotor. El objetivo principal es evaluar la tendencias en la electrificación del transporte y su relación con la reducción de emisiones derivadas del transporte por carretera.

Para ello, se construyeron tres dataframes principales a partir de fuentes oficiales europeas (Eurostat), que se inspeccionaron inicialmente en crudo con el fin de comprender su estructura y diagnosticar la calidad del contenido, luego se limpiaron, normalizaron y reestructuraron para que estén listos para su respectivo análisis visual e interpretación.

---

## 🛠️ Preparación de los datos

1. 🌍 __df_greenhouse_gases__ (Greenhouse gas emissions by source sector)   
Contiene las emisiones anuales de gases de efecto invernadero en Europa, las emisiones están clasificada y agrupadas sus sectores fuentes (transporte, industria, agricultura, etc.).

    Procesamiento:
    - Eliminar columnas vacias que no aportan información útil al análisis. 
    - Agrupar de categorías principales a traves de sus subcategorías.
    - Crear nuevas columnas que incluyan los ítems informativos en sus recuentos.
    - Renombrado de columnas.

2. 🚗✨ __df_new_cars__ (New passenger cars by type of motor energy)   
Recoge el número de matriculaciones anuales de vehículos nuevos de cada país de Europa, distinguiendo entre tipos de motorización.

    Procesamiento:
    - Filtro geográfico de los 27 países que pertenecen a la Unión Europea (UE-27).
    - Reconstrucción del total para la UE recalculando los valores por año.
    - Renombrado y limpieza de columnas.
    - Reagrupación por categorías energéticas (alternativos, electrificados).

3. 🚙 __df_cars_park__ (Passenger cars, by type of motor energy)   
Representa el parque automotor total en circulación, clasificados según el tipo de energía motriz.

    Procesamiento:
    - Filtro geográfico de los 27 países que pertenecen a la Unión Europea (UE-27).
    - Reconstrucción del total para la UE recalculando los valores por año.
    - Renombrado y limpieza de columnas.
    - Reagrupación por categorías energéticas (alternativos, electrificados).

---

## 📈 Enfoque analítico

El análisis se centra en examinar las correlaciones entre tres ejes:
- La evolución de las emisiones netas totales de los gases de efecto invernadero desde 1990 hasta 2022, y profundizar en las emisiones del transporte por carreteras.
- La evolución de las matriculaciones de nuevos vehículos, ahondando en el crecimiento de los vehiculos electrificados.
- La composición general del parque automotor, y concluir si hubo una reducción progresiva de las emisiones de GEI asociadas al transporte por carretera.

A través de las visualizaciones, se explora cómo la transición hacia vehículos electrificados impacta en las emisiones del transporte por carreteras, y cómo el ritmo de electrificación del parque vehicular se compara con la composición total del parque automotiz.

---

## ⚙️ Herramientas utilizadas

- Python 3.12.5
- Pandas para la manipulación y limpieza de datos.
- Pandas, Mathplotlib y Seaborn para las visualizaciones.
- Plotly.express para las visualizaciones interactivas.
- Jupyter Notebooks para el desarrollo y la documentación del proceso.

---

## 📊 Resultados y conclusiones

El análisis de los datos de Eurostat revela una disminución significativa en las emisiones de gases de efecto invernadero (GEI) en Europa durante las últimas tres décadas y a la vez un crecimiento exponencial en la electrificación del transporte.

1. Tendencias en las emisiones de GEI

    - Desde 1990 hasta 2022, las emisiones totales de GEI en la Unión Europea se redujeron aproximadamente un 32 %.
    - Sin embargo, dentro del sector combustión, el mayor contribuyente fue industrias energéticas con aproximadamente el 34 % de las emisiones, seguido del sector transporte que representa cerca del 31 % de las emisiones totales en 2022.
    - Dentro de transporte, el transporte por automóviles (turismos) sigue siendo el principal responsable con alrededor del 56 % del total del transporte.

2. Electrificación del parque automotor

    - La matriculacion de vehículos electrificados mostro un crecimiento exponencial, pasando de 129 mil coches en 2013 a cerca de 4.2 millones en 2022, un incremento del 3128 % en nueve años.
    - El parque automotor electrificado (vehículos en circulación) continua representando aún una fracción menor del total, pero con una tendencia claramente ascendente. Entre 2013 y 2022, la participación de los vehículos eléctricos aumentó de apenas 0.25 % al 5.57 %.

3. Correlación entre electrificación y emisiones

    - A medida que aumentó la cuota de vehículos electrificados y se redujo la matriculación de coches de combustión interna las emisiones del transporte por carretera comenzaron a estabilizarse y posteriormente a descender, con una caida significativa en 2020 debido a la poca movilización que hubo durante la pandemia. Las emisiones no han vuelto a subir hasta los niveles prepandemia, lo que sugiere una correlación inversa entre estas variables.

4. Conclusión general

    La transición hacia un parque automotor electrificado ya muestra impactos positivos en la reducción de emisiones del transporte, aunque el ritmo de sustitución del parque aún es insuficiente para alcanzar los objetivos de neutralidad climática de 2050. El análisis indica que la aceleración de la electrificación será clave para una reducción sostenida de GEI en la próxima década.

---

## 📁 Próximos pasos

- Incorporar proyecciones hasta 2030 utilizando modelos de regresión o series temporales.
- Desarrollar un dashboard interactivo para la exploración dinámica de los datos.

---
---
