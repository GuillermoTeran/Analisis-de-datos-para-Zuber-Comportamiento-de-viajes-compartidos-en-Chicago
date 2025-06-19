# Análisis de datos para Zuber: Comportamiento de viajes compartidos en Chicago

## ES Español

**Rol:** Analista de Datos  
**Tecnologías:** SQL (PostgreSQL), Python (pandas, matplotlib, seaborn, scipy), Jupyter Notebook

### Descripción del proyecto  
Como analista de datos para Zuber, una nueva empresa de viajes compartidos en Chicago, me encargué de identificar patrones clave en los datos de transporte urbano. El objetivo fue comprender mejor las preferencias de los pasajeros, el desempeño de los competidores y el impacto del clima en los viajes, con un enfoque particular en noviembre de 2017. El análisis incluyó integración de múltiples fuentes, consultas SQL, visualización en Python y pruebas estadísticas.

### Objetivos del análisis  
- Analizar el comportamiento de los competidores de Zuber en términos de volumen de viajes.  
- Identificar los barrios más populares para dejar pasajeros.  
- Investigar si el clima lluvioso afecta la duración de los viajes desde el centro de Chicago (Loop) hasta el Aeropuerto O'Hare.  
- Proveer conclusiones accionables para estrategias de mercado y operaciones.

### Paso 1: Análisis de clima en Chicago  
Se recopiló información externa sobre condiciones meteorológicas durante noviembre 2017. Clave para vincular clima y comportamiento de viaje, especialmente sábados.

### Paso 2: Análisis SQL  
Consultas destacadas:  
- Número de viajes por empresa (15–16 nov): Flash Cab y Taxi Affiliation Services lideraron.  
- Viajes de empresas "Yellow" o "Blue" (1–7 nov): análisis de marcas tradicionales.  
- Agrupación de empresas: principales agrupadas y resto como "Other" para simplificar análisis.  
Resultado: alta concentración de mercado en pocas compañías.

### Paso 3: Hipótesis sobre clima y duración de viajes  
Pregunta: ¿Cambia duración promedio de viajes Loop → O’Hare en sábados lluviosos?  
- Clasificación clima: "Bad" (lluvia/tormenta) y "Good".  
- Selección de viajes solo sábados entre Loop (neighborhood_id 50) y O'Hare (neighborhood_id 63).  
- Asociación viajes con condiciones meteorológicas.

### Paso 4: Análisis exploratorio en Python  
Trabajé con tres datasets exportados desde SQL:  
1. Empresas de taxi (project_sql_result_01.csv): número de viajes por empresa; Flash Cab líder.  
2. Barrios de destino (project_sql_result_04.csv): top 10 barrios con más viajes, centrados en zonas turísticas y céntricas.  
3. Duración y clima (project_sql_result_07.csv): base para prueba de hipótesis.

### Paso 5: Prueba de hipótesis con Python  
Hipótesis:  
- H₀: duración media no cambia entre sábados con buen y mal clima.  
- H₁: duración media cambia.  
Método: t-test para dos muestras independientes, α = 0.05.  
Resultado: p > 0.05, no se rechaza H₀.  
Conclusión: no hay diferencias significativas en duración entre sábados lluviosos y no lluviosos.

### Conclusiones generales  
- Zuber enfrenta competencia fuerte de empresas establecidas (Flash Cab).  
- Destinos concentrados en barrios céntricos.  
- Clima lluvioso no afecta significativamente duración Loop → O’Hare los sábados; patrón podría variar en otras fechas o rutas.

### Herramientas utilizadas  
- SQL (PostgreSQL) para consultas complejas y agrupación.  
- Python: pandas, matplotlib, seaborn, scipy para análisis y visualización.  
- Jupyter Notebook para documentación y presentación.

### Impacto del proyecto  
Este análisis ayudó a Zuber a entender la dinámica del mercado en Chicago, identificar áreas de alta demanda y evaluar la influencia del clima en la operación, sustentando decisiones estratégicas sobre posicionamiento, competencia y planificación.

---

# Data analysis for Zuber: Ride-sharing behavior in Chicago

## US English

**Role:** Data Analyst  
**Technologies:** SQL (PostgreSQL), Python (pandas, matplotlib, seaborn, scipy), Jupyter Notebook

### Project description  
As a data analyst for Zuber, a new ride-sharing company in Chicago, I was tasked with identifying key patterns in urban transportation data. The goal was to better understand passenger preferences, competitor performance, and the impact of weather on travel, focusing on November 2017. The analysis included integrating multiple data sources, SQL queries, Python visualization, and statistical testing.

### Analysis objectives  
- Analyze the behavior of Zuber's competitors by trip volume.  
- Identify the most popular neighborhoods for drop-offs.  
- Investigate whether rainy weather affects trip duration from downtown Chicago (Loop) to O'Hare Airport.  
- Provide actionable conclusions for market and operational strategies.

### Step 1: Chicago weather analysis  
Collected external data on weather conditions in November 2017. Key to link weather and travel behavior, especially Saturdays.

### Step 2: SQL analysis  
Notable queries:  
- Trips per company (Nov 15–16): Flash Cab and Taxi Affiliation Services led.  
- Trips by “Yellow” or “Blue” companies (Nov 1–7): analysis of traditional brands.  
- Company grouping: main companies grouped, others as “Other” for market share simplification.  
Result: high market concentration among few companies.

### Step 3: Hypothesis about weather and trip duration  
Key question: Does average trip duration from Loop to O'Hare change on rainy Saturdays?  
- Weather categorized as “Bad” (rain/storm) and “Good.”  
- Selected trips on Saturdays between Loop (neighborhood_id 50) and O'Hare (neighborhood_id 63).  
- Linked trips with weather conditions.

### Step 4: Exploratory analysis in Python  
Used three datasets from SQL:  
1. Taxi companies (project_sql_result_01.csv): trip counts by company; Flash Cab leading.  
2. Destination neighborhoods (project_sql_result_04.csv): top 10 neighborhoods by trips, mainly downtown and tourist areas.  
3. Trip duration and weather (project_sql_result_07.csv): base for hypothesis testing.

### Step 5: Hypothesis testing with Python  
Hypotheses:  
- H₀: average trip duration does not change between good and bad weather Saturdays.  
- H₁: average trip duration changes.  
Method: t-test for two independent samples, α = 0.05.  
Result: p-value > 0.05, null hypothesis not rejected.  
Conclusion: no significant difference in trip duration between rainy and non-rainy Saturdays.

### General conclusions  
- Zuber faces strong competition from established companies like Flash Cab.  
- Destination patterns concentrated in downtown neighborhoods.  
- Rainy weather does not significantly affect Loop → O'Hare trip duration on Saturdays; pattern may vary on other dates or routes.

### Tools used  
- SQL (PostgreSQL) for complex queries and grouping.  
- Python: pandas, matplotlib, seaborn, scipy for analysis and visualization.  
- Jupyter Notebook for documentation and presentation.

### Project impact  
This analysis helped Zuber better understand Chicago’s market dynamics, identify high-demand areas, and assess weather influence on operations, supporting strategic decisions about positioning, competition, and planning.
