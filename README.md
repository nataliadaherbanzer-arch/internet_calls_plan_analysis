# Internet & calls plan analysis
Este proyecto analiza el comportamiento de los usuarios de la compañía de telecomunicaciones Megaline. El objetivo principal es determinar cuál de los dos planes tarifarios (Surf y Ultimate) genera mayores ingresos, con el fin de ajustar el presupuesto de publicidad basado en evidencia estadística.

El análisis abarca el procesamiento de datos de consumo (llamadas, SMS, navegación) de 500 usuarios durante el año 2018.

## Stack Tecnológico
Lenguaje: Python 

Librerías principales: Pandas (manipulación), Matplotlib / Seaborn (visualización), SciPy (pruebas estadísticas) y NumPy.

## Preparación de datos para el análisis

El análisis integra cinco fuentes de datos distintas para construir un perfil consolidado por usuario/mes:

Users: Información demográfica y plan suscrito.

Calls: Registro detallado de duraciones y fechas.

Messages: Conteo de SMS enviados.

Internet: Tráfico de datos en megabytes.

Plans: Condiciones comerciales de cada tarifa.

## Metodología de Procesamiento
Para asegurar la integridad de los insights, se realizaron las siguientes tareas de Data Engineering:

Conversión de tipos: Ajuste de formatos de fecha y redondeo de valores (Megaline redondea segundos a minutos y MB a GB según política comercial).

Tratamiento de nulos: Identificación de usuarios sin consumo en ciertos servicios y gestión de fechas de cancelación.

Agregación: Construcción de un DataFrame maestro con ingresos mensuales calculados (Tarifa básica + excedentes).

## Análisis Exploratorio (EDA)
Se analizaron las variables clave para entender la distribución del consumo:

- Llamadas: Distribución de minutos y frecuencia mensual.

- Mensajería: Análisis de la relevancia del SMS en la era digital.

- Internet: Identificación de patrones de consumo de datos.

- Ingresos: Comparativa visual mediante diagramas de caja (Boxplots) para detectar outliers en el gasto de usuarios.


## Pruebas de Hipótesis Estadísticas

Se aplicó el método de prueba t de Student para muestras independientes con un nivel de significancia ($\alpha$) del 5%.

## Hipótesis 1: Diferencia de ingresos entre planes

- H₀:El ingreso promedio de los usuarios de los planes Ultimate y Surf es igual.

- H₁: El ingreso promedio de los usuarios de los planes Ultimate y Surf es diferente.


## Hipótesis 2: Impacto geográfico (NY-NJ vs. Otros)

- H₀: El ingreso promedio de los usuarios en el área de NY-NJ es igual al de otras regiones.

- H₁: El ingreso promedio de los usuarios en el área de NY-NJ es diferente al de otras regiones.

## Conclusionens y recomendaciones 

Mi recomendación para el equipo de Marketing es priorizar la promoción del Plan Ultimate.

Aunque el Plan Surf parece popular, el Plan Ultimate ofrece un ingreso más alto y predecible para la empresa. Además, no es necesario crear campañas específicas para Nueva York o Nueva Jersey, ya que el comportamiento de consumo es bastante estándar en todo el país.
