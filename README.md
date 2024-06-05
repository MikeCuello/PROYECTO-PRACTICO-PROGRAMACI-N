# Análisis de Datos de Ventas de Videojuegos
## Descripción del Proyecto
Este proyecto se centra en el análisis de un conjunto de datos de ventas de videojuegos. Utilizando un cuaderno de Jupyter, se han realizado diversas tareas de análisis y visualización para extraer información valiosa sobre las tendencias y patrones en las ventas de videojuegos a nivel global.
## Contenido del Proyecto
El proyecto incluye los siguientes archivos:

•	Video_Games_Sales_as_at_22_Dec_2016.csv: El conjunto de datos que contiene información sobre las ventas de videojuegos hasta diciembre de 2016.

•	Proyecto_de_analitica_de_datos.ipynb: Un cuaderno de Jupyter que documenta el proceso de análisis de datos, incluyendo la carga, limpieza, y visualización de los datos.
## Estructura del Conjunto de Datos
El conjunto de datos contiene las siguientes columnas:

•	Name: Nombre del videojuego.

•	Platform: Plataforma de la consola.

•	Year_of_Release: Año de lanzamiento.

•	Genre: Género del videojuego.

•	Publisher: Empresa que publicó el videojuego.

•	NA_Sales, EU_Sales, JP_Sales, Other_Sales: Ventas en Norteamérica, Europa, Japón y otras regiones (en millones).

•	Global_Sales: Ventas globales totales (en millones).

•	Critic_Score: Puntuación de críticos.

•	Critic_Count: Número de críticas.

•	User_Score: Puntuación de usuarios.

•	User_Count: Número de usuarios que puntuaron.

•	Developer: Desarrollador del videojuego.

•	Rating: Clasificación por edades.
## Instalación
Para ejecutar el cuaderno de Jupyter, necesitarás instalar las siguientes bibliotecas:

pip install pandas numpy matplotlib seaborn

## Uso
El cuaderno de Jupyter incluye varias secciones clave:
1.Carga y Visualización de Datos: Cargar el conjunto de datos y mostrar una vista previa.

import pandas as pd

df = pd.read_csv('Video_Games_Sales_as_at_22_Dec_2016.csv')

df.head()

2.	Limpieza de Datos: Identificación y manejo de valores nulos.

columnas_conservadas = ['Name', 'Year_of_Release', 'Platform', 'Genre', 'NA_Sales', 'EU_Sales', 'JP_Sales', 'Other_Sales', 'Global_Sales']

df_filtrado = df[columnas_conservadas]

df_filtrado.isnull().sum()

3.	Análisis Exploratorio de Datos (EDA): Análisis descriptivo y visualizaciones para entender las tendencias y patrones en los datos.
		
import matplotlib.pyplot as plt

import seaborn as sns

sns.barplot(x='Genre', y='Global_Sales', data=df_filtrado)

plt.show()

## Resultados
Algunos de los resultados clave del análisis incluyen:

Ventas por Género: Identificación de los géneros de videojuegos más vendidos.

Ventas por Plataforma: Análisis de las plataformas con mayores ventas.

Tendencias Anuales: Evolución de las ventas de videojuegos a lo largo de los años.

Impacto de las Críticas: Relación entre las puntuaciones de críticos y usuarios con las ventas.

## Contribuciones
Las contribuciones son bienvenidas. Por favor, abre un 'issue' para discutir cualquier cambio que desees realizar.
## Licencia
Este proyecto está bajo la Licencia MIT. Consulta el archivo LICENSE para más detalles.


## Contacto
Para cualquier consulta, puedes contactar a [tu nombre o tu email].
