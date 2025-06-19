# Análisis de datos para Zuber: Comportamiento de viajes compartidos en Chicago

## ES Español

Descripción del proyecto:

Como analista de datos para Zuber, una nueva empresa de viajes compartidos en Chicago, me encargué de identificar patrones clave en los datos de transporte urbano. El objetivo fue comprender mejor las preferencias de los pasajeros, el desempeño de los competidores y el impacto del clima en los viajes, con un enfoque particular en el mes de noviembre de 2017.

El análisis incluyó la integración de múltiples fuentes de datos, consultas SQL, visualización en Python y pruebas estadísticas.

## Objetivos del análisis:
Analizar el comportamiento de los competidores de Zuber en términos de volumen de viajes.

Identificar los barrios más populares para dejar pasajeros.

Investigar si el clima lluvioso afecta la duración de los viajes desde el centro de Chicago (Loop) hasta el Aeropuerto O'Hare.

Proveer conclusiones accionables para estrategias de mercado y operaciones.

## Paso 1: Análisis de clima en Chicago
Se recopiló información desde un recurso externo que contenía condiciones meteorológicas en Chicago durante noviembre de 2017. Este análisis fue clave para vincular el clima con el comportamiento de viaje, especialmente los días sábado.

## Paso 2: Análisis SQL
Consultas destacadas:

Número de viajes por empresa (15–16 nov): Identifiqué las empresas más activas, destacándose Flash Cab y Taxi Affiliation Services.

Viajes de empresas "Yellow" o "Blue" (1–7 nov): Analicé el comportamiento de marcas tradicionales.

Agrupación de empresas: Agrupé las empresas principales y clasifiqué al resto como "Other" para simplificar el análisis de participación en el mercado.

Resultado: Se evidenció una alta concentración del mercado en unas pocas compañías.

## Paso 3: Hipótesis sobre clima y duración de viajes
Pregunta clave:

¿Cambia la duración promedio de los viajes desde Loop hasta O’Hare en sábados lluviosos?

Pasos seguidos:

Clasifiqué el clima en dos categorías: "Bad" (lluvia/tormenta) y "Good".

Seleccioné solo los viajes entre Loop (neighborhood_id 50) y O'Hare (neighborhood_id 63) realizados los sábados.

Vinculé cada viaje con las condiciones meteorológicas correspondientes.

## Paso 4: Análisis exploratorio en Python
Trabajé con tres datasets exportados desde SQL:

1. Empresas de taxi (project_sql_result_01.csv):
Visualización del número de viajes por empresa.

Flash Cab lideró por amplio margen en volumen de viajes.

2. Barrios de destino (project_sql_result_04.csv):
Identifiqué los 10 barrios principales en términos de viajes finalizados.

Se observaron zonas céntricas y turísticas entre las más frecuentadas.

3. Duración de viajes y clima (project_sql_result_07.csv):
Dataset base para la prueba de hipótesis.

## Paso 5: Prueba de hipótesis con Python
Hipótesis formuladas:

H₀ (nula): La duración media de los viajes no cambia entre sábados con buen y mal clima.

H₁ (alternativa): La duración media de los viajes sí cambia entre sábados con buen y mal clima.

Método:

Prueba de hipótesis para dos muestras independientes (t-test).

Nivel de significancia α = 0.05.

Resultado:

El valor p fue mayor que 0.05, por lo tanto no se rechaza la hipótesis nula.

Conclusión: No se encontraron diferencias significativas en la duración de los viajes entre sábados lluviosos y no lluviosos.

## Conclusiones generales:
Zuber enfrenta fuerte competencia de empresas establecidas como Flash Cab.

Los patrones de destino muestran una alta concentración en barrios céntricos.

El clima lluvioso no parece afectar significativamente la duración de los viajes desde el Loop a O’Hare los sábados, aunque este patrón podría variar en otras fechas o trayectos.

## Herramientas utilizadas:
SQL (PostgreSQL): consultas complejas y agrupación de datos.

Python: pandas, matplotlib, seaborn, scipy.

Jupyter Notebook: para documentación y visualización del análisis.

## Impacto del proyecto:
Este análisis ayudó a Zuber a entender mejor la dinámica del mercado en Chicago, identificar áreas de alta demanda, y evaluar la influencia del clima sobre su operación. Los resultados permiten fundamentar decisiones estratégicas relacionadas con el posicionamiento, la competencia y la planificación operativa.


# Data analysis for Zuber: Ride-sharing behavior in Chicago

## US English

Project description:

As a data analyst for Zuber, a new ride-sharing company in Chicago, I was tasked with identifying key patterns in urban transportation data. The goal was to better understand passenger preferences, competitor performance, and the impact of weather on travel, with a particular focus on the month of November 2017.

The analysis included integrating multiple data sources, SQL queries, visualization in Python, and statistical testing.

## Analysis objectives:
Analyze the behavior of Zuber's competitors in terms of trip volume.

Identify the most popular neighborhoods for dropping off passengers.

Investigate whether rainy weather affects the duration of trips from downtown Chicago (Loop) to O'Hare Airport.

Provide actionable conclusions for market and operations strategies.

## Step 1: Chicago weather analysis
Information was collected from an external resource containing weather conditions in Chicago during November 2017. This analysis was key to linking weather to travel behavior, especially on Saturdays.

## Step 2: SQL analysis
Notable queries:

Number of trips per company (Nov. 15–16): I identified the most active companies, with Flash Cab and Taxi Affiliation Services standing out.

Trips by “Yellow” or “Blue” companies (Nov. 1–7): I analyzed the behavior of traditional brands.

Company grouping: I grouped the main companies and classified the rest as “Other” to simplify the analysis of market share.

Result: There was evidence of high market concentration among a few companies.

## Step 3: Hypothesis about weather and trip duration
Key question:

Does the average duration of trips from Loop to O'Hare change on rainy Saturdays?

Steps taken:

I classified the weather into two categories: “Bad” (rain/storm) and “Good.”

I selected only trips between Loop (neighborhood_id 50) and O'Hare (neighborhood_id 63) made on Saturdays.

I linked each trip to the corresponding weather conditions.

## Step 4: Exploratory analysis in Python
I worked with three datasets exported from SQL:

1. Taxi companies (project_sql_result_01.csv):
Visualization of the number of trips per company.

Flash Cab led by a wide margin in trip volume.

2. Destination neighborhoods (project_sql_result_04.csv):
I identified the top 10 neighborhoods in terms of completed trips.

Downtown and tourist areas were among the most frequented.

3. Trip duration and weather (project_sql_result_07.csv):
Base dataset for hypothesis testing.

## Step 5: Hypothesis testing with Python
Hypotheses formulated:

H₀ (null): The average trip duration does not change between Saturdays with good and bad weather.

H₁ (alternative): The average trip duration does change between Saturdays with good and bad weather.

Method:

Hypothesis testing for two independent samples (t-test).

Significance level α = 0.05.

Result:

The p-value was greater than 0.05, therefore the null hypothesis is not rejected.

Conclusion: No significant differences were found in trip duration between rainy and non-rainy Saturdays.

## General conclusions:
Zuber face stiff competition from established companies such as Flash Cab.

Destination patterns show a high concentration in downtown neighborhoods.

Rainy weather does not appear to significantly affect trip duration from the Loop to O'Hare on Saturdays, although this pattern may vary on other dates or routes.

## Tools used:
SQL (PostgreSQL): complex queries and data grouping.

Python: pandas, matplotlib, seaborn, scipy.

Jupyter Notebook: for documentation and visualization of the analysis.

## Project impact:
This analysis helped Zuber better understand market dynamics in Chicago, identify areas of high demand, and assess the influence of weather on its operations. The results provide a basis for strategic decisions related to positioning, competition, and operational planning.

