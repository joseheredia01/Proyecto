# Calculo de temperatura máxima y mínima promedio mensual de Coquimatán, Col. del periodo 1990 a 2017 con Python

**FACULTAD DE INGENIERIA CIVIL**\
**INGENIERO TOPOGRAFO GEOMATICO**\
**Autores**:\
Maximiliano Amezcua Delgado\
José Guadalupe Heredia Aguilar\
Melany Jexemany Aquino Orozco\
Lari Naum Larios Santillán\
**Grado y Grupo**: 3ºB\
**Asesor**: Sebastián Gonzales Zepeda;\
Coquimatlán, Colima a 29 nov 2023

# Resumen
En este proyecto lo que tenemos básicamente es una tabla de datos de Excel en la cual vienen los datos sobre cuál fue la temperatura máxima promedio mensual y la mínima promedio mensual de Coquimatlán desde 1990 hasta el 2017.
Esto para saber si es que la temperatura promedio máxima o mínima ha aumentado en los últimos años o de lo contrario si el planeta se ha enfriado un poco más, aunque es obvio que lo más probable es que se haya calentado más.

# Introducción
En este proyecto lo que debemos de realizar es un programa en el cual nos pueda graficar sobre un archivo de Excel en el cual están muchos datos sobre cuál fue la temperatura promedia mensual sobre los años de 1990 – 2017, puede ser que el programa nos arroje datos como lo son, cual es el valor que más se repite (moda), cual es el promedio de todo, cual es el promedio de un año, la frecuencia, el valor mínimo, el valor máximo, entre otras cosas.
La obtención de información no siempre es tan sencilla como parece y esto lo pudimos constatar porque nuestro proyecto original hablaba de la deserción de alumnos de topógrafo geomático de primero a tercer semestre, sin embargo, nos fue complicado obtener esta información debido a problemas o situaciones ajenas que nosotros no podíamos solventar. 
Por eso decidimos cambiar al proyecto de temperatura máxima y mínima mensual del municipio de Coquimatlán, Colima desde el año 1990 hasta el año 2017, lo elegimos para saber si hubo algún aumento de la temperatura promedio durante estos 27 años, si es que el calentamiento global afecto en eso o si realmente sigue igual, entre otras cosas.
Y aprovechar que estos datos nos sirven realmente a nosotros (locales), ya que es información del lugar donde vivimos y podemos comprobar si es cierto que la temperatura ha aumentado.
La información fue muy fácil de recabar ya que todos estos datos venían organizados en una tabla del Servicio Meteorológico Nacional y solo se trasladaron los datos que estaban en esa tabla y se organizaron en una tabla de Excel.

# Desarrollo
Básicamente lo que vamos a hacer en este proyecto es saber cuál es la temperatura máxima y mínima promedio mensual de Coquimatlán desde el año de 1990 hasta 2017, en este proyecto lo que buscamos hacer es realizar gráficas donde se muestren los datos de cuáles fueron las temperaturas promedio de cada año, así como también la temperatura más alta, saber cuáles son las temperaturas que más se frecuentan en este rango de años, entre otras cosas.
Todo esto se saca o se sacó desde la página de servicio meteorológico nacional en la parte del historial de temperaturas promedio, en este caso de la localidad de Coquimatlán, de ahí los datos se traslada a una tabla de Excel en los cuales serán procesados para poder realizar lo que es el código que esta materia y el maestro necesitan para que puedan ser evaluadas nuestra cuarta parcial.

# Manejo de datos
Para el manejo de datos, lo que realizaremos es una tabla de Excel en la cual pondremos todos nuestros datos ahí, y después con un código de Python mandaremos a llamar todos los datos para así saber cuáles son las respuestas de las preguntas que tenemos como base.
![](https://github.com/joseheredia01/Proyecto/blob/main/imagenes/manejo%20de%20datos%201.jpg?raw=true)

# Codigos
#Proyecto de Programación\
/## Cargar Librerías
%config IPCompleter.greedy=True
import pandas as pd
import numpy as np
import xlrd
import seaborn as sb
import matplotlib.pyplot as plt
from matplotlib.ticker import PercentFormatter
#Cargar base de datos
from google.colab import files
from google.colab import drive
drive.mount('/content/drive')
import pandas as pd
df = pd.read\_excel("/content/drive/MyDrive/Colab Notebooks/Programacion 2/Parcial 4/Temperatura Maxima y Minima Promedio Mensual de Coquimatlán.xlsx")
df.shape
#Tamaño de los datos
print('El tamaño de los datos en filas y columnas es de ',df.shape)
pd.read\_excel("/content/drive/MyDrive/Colab Notebooks/Programacion 2/Parcial 4/Temperatura Maxima y Minima Promedio Mensual de Coquimatlán.xlsx")
df.dtypes
print('\nLos datos son de tipo:\n',df.dtypes)
# 
![](https://github.com/joseheredia01/Proyecto/blob/main/imagenes/Codigo%201.jpg?raw=true)
#
Temperatura Maxima Promedio Mensual 1990 - 2017
Promedio = (39.13191667 + 39.57891667 + 34.94366667 + 33.7525 + 32.44941667 + 31.35691667 + 33.82208333 + 33.61225 + 33.65366667 + 33.67825 + 33.55075 + 34.01283333 + 34.26741667 + 34.2295 + 33.84925 + 34.02675 + 34.50808333 + 34.49625 + 33.84725 + 34.47433333 + 33.31608333 + 34.11441667 + 32.48825 + 32.40975 + 33.2305 + 33.38466667 + 33.45941667 + 33.05041667)/27
print ("El promedio de la temperatura maxima promedio total es de",Promedio)
import statistics
data = [39.13191667 , 39.57891667 , 34.94366667 , 33.7525 , 32.44941667 , 31.35691667 , 33.82208333 , 33.61225 , 33.65366667 , 33.67825 , 33.55075 , 34.01283333 , 34.26741667 , 34.2295 , 33.84925 , 34.02675 , 34.50808333 , 34.49625 , 33.84725 , 34.47433333 , 33.31608333 , 34.11441667 , 32.48825 , 32.40975 , 33.2305 , 33.38466667 , 33.45941667 , 33.05041667]
\# Calcula la moda utilizando la función mode() de statistics
mode = statistics.mode(data)
print("La Moda es de", mode)
datos = [39.13191667 , 39.57891667 , 34.94366667 , 33.7525 , 32.44941667 , 31.35691667 , 33.82208333 , 33.61225 , 33.65366667 , 33.67825 , 33.55075 , 34.01283333 , 34.26741667 , 34.2295 , 33.84925 , 34.02675 , 34.50808333 , 34.49625 , 33.84725 , 34.47433333 , 33.31608333 , 34.11441667 , 32.48825 , 32.40975 , 33.2305 , 33.38466667 , 33.45941667 , 33.05041667]
\# Calcular la desviación estándar utilizando NumPy
desviacion\_estandar = np.std(datos)
print("La desviación estándar es de", desviacion\_estandar)
#Definimos una lista con años como string
años = ['1990', '1991', '1992', '1993', '1994', '1995', '1996', '1997', '1998', '1999', '2000', '2001', '2002', '2003', '2004', '2005', '2006', '2007', '2008', '2009', '2010', '2011', '2012', '2013', '2014', '2015', '2016', '2017']
#Definimos una lista
Temperaturas = [39.13191667 , 39.57891667 , 34.94366667 , 33.7525 , 32.44941667 , 31.35691667 , 33.82208333 , 33.61225 , 33.65366667 , 33.67825 , 33.55075 , 34.01283333 , 34.26741667 , 34.2295 , 33.84925 , 34.02675 , 34.50808333 , 34.49625 , 33.84725 , 34.47433333 , 33.31608333 , 34.11441667 , 32.48825 , 32.40975 , 33.2305 , 33.38466667 , 33.45941667 , 33.05041667]
fig, ax = plt.subplots()
#Colocamos una etiqueta en el eje Y
ax.set\_ylabel('Temperaturas')
#Colocamos una etiqueta en el eje X
ax.set\_title('Temperaturas Maximas Promedio Anual')
#Creamos la grafica de barras
plt.bar(años, Temperaturas)
plt.savefig('barras\_simple.png')
#Finalmente mostramos la grafica con el metodo show()
plt.show()
#
![](https://github.com/joseheredia01/Proyecto/blob/main/imagenes/Codigo%202.0.jpg?raw=true)
![](https://github.com/joseheredia01/Proyecto/blob/main/imagenes/Codigo%202.1.jpg?raw=true)
# Resultados
![](https://github.com/joseheredia01/Proyecto/blob/main/imagenes/grafica1.jpg?raw=true)
![](https://github.com/joseheredia01/Proyecto/blob/main/imagenes/grafica2.jpg?raw=true)
![](https://github.com/joseheredia01/Proyecto/blob/main/imagenes/grafica3.jpg?raw=true)
![](https://github.com/joseheredia01/Proyecto/blob/main/imagenes/grafica4.jpg?raw=true)
# Conclusión
La experiencia de llevar a cabo un proyecto inicial sobre la falta de estudiantes en una carrera especifica y las dificultades para obtener la información necesaria destacó la complejidad en la recolección de datos.

La transición hacia un nuevo proyecto que se enfocó en el análisis de las temperaturas máximas y mínimas mensuales en Coquimatlán, Colima, desde 1990 hasta 2017 permitió abordar un tema de relevancia local, como el cambio climático y sus posibles efectos en la región, utilizando datos fácilmente accesibles de fuentes confiables, como el Servicio Meteorológico Nacional.

La importancia de la disponibilidad y accesibilidad de la información se destaca por la facilidad con la que se obtuvieron los datos para el segundo proyecto. Este cambio no solo dio a la comunidad local la oportunidad de investigar un tema relevante, sino que también permitió una verificación precisa y localizable de los efectos del cambio climático en el área.

En conclusión, lidiar con problemas de obtención de datos en el proyecto inicial llevó a un cambio reflexivo y productivo hacia un proyecto nuevo y apropiado. Este proceso destaca la importancia de la adaptabilidad y la flexibilidad en la investigación, así como la relevancia de la información local y su utilidad para comprender y abordar problemas importantes de la comunidad.
# Póster científico
![](https://github.com/joseheredia01/Proyecto/blob/main/imagenes/Poster%20Cientifico%20Proyecto%20Progra_page-0001.jpg?raw=true)
