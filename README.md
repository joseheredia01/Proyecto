# Datos

**FACULTAD DE INGENIERIA CIVIL**;
**INGENIERO TOPOGRAFO GEOMATICO**;
**"Temperatura Máxima y Mínima Promedio Mensual en Coquimatlán en 1990 - 2017”**;
**Maestro**: Sebastián Gonzales Zepeda;
**Autores**: 
Maximiliano Amezcua Delgado,
José Guadalupe Heredia Aguilar,
Melany Jexemany Aquino Orozco, y 
Lari Naum Larios Santillán; 
**Grado y Grupo**: 3ºB
Coquimatlán, Colima a 29/11/2023

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
![](https://github.com/joseheredia01/Proyecto/blob/main/manejo%20de%20datos%201.jpg?raw=true)

# Codigo
#Proyecto de Programación
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
