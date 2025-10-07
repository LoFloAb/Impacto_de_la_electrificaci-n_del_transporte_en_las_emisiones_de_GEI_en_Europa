___
___
# **Impacto de la electrificación del transporte en las emisiones de GEI en Europa**
___
## 📘 Descripción 

Este proyecto analiza la evolución de las emisiones de gases de efecto invernadero (GEI) en Europa, los cambios en la matriculación de nuevos vehículos y la evolución del parque automotor. El objetivo principal es evaluar la tendencias en la electrificación del transporte y su relación con la reducción de emisiones derivadas del transporte por carretera.

Para ello, se construyeron tres dataframes principales a partir de fuentes oficiales europeas (Eurostat), que se inspeccionaron inicialmente en crudo con el fin de comprender su estructura y diagnosticar la calidad del contenido, luego se limpiaron, normalizaron y reestructuraron para que estén listos para su respectivo análisis visual e interpretación.
___
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
___
## 📈 Enfoque analítico

El análisis se centra en examinar las correlaciones entre tres ejes:
- La evolución de las emisiones netas totales de los gases de efecto invernadero desde 1990 hasta 2022, y profundizar en las emisiones del transporte por carreteras.
- La evolución de las matriculaciones de nuevos vehículos, ahondando en el crecimiento de los vehiculos electrificados.
- La composición general del parque automotor, y escrutar en hubo una reducción progresiva de las emisiones de GEI asociadas al transporte por carretera.

A través de las visualizaciones, se explora cómo la transición hacia vehículos electrificados impacta en las emisiones del transporte por carreteras, y cómo el ritmo de electrificación del parque vehicular se compara con la composición total del parque automotiz.
___
## ⚙️ Herramientas utilizadas

- Python 3.12.5
- Pandas para la manipulación y limpieza de datos.
- Pandas, Mathplotlib y Seaborn para las visualizaciones.
- Plotly.express para las visualizaciones interactivas.
- Jupyter Notebooks para el desarrollo y la documentación del proceso.