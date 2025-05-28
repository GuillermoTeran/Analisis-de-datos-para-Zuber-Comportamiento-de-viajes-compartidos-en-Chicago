# Análisis de datos para Zuber: Comportamiento de viajes compartidos en Chicago
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

