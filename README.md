# Análisis espacial de potencial inicial de gas en Virginia

![Tamaño](https://github-size-badge.herokuapp.com/andresarguedas/proyecto-final-espacial.svg) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) [![License: CC BY 4.0](https://licensebuttons.net/l/by/4.0/80x15.png)](https://creativecommons.org/licenses/by/4.0/deed.es)

## Resumen

Este repositorio contiene el código y datos de la presentación sobre el proyecto final del curso SP-1649 Tópicos de Estadística Espacial Aplicada: **Análisis espacial de potencial inicial de gas en Virginia**, desarrollado por Miguel Coto y Esteban Vargas, como parte de la Maestría en Estadística de la Universidad de Costa Rica. 

- [Análisis espacial de potencial inicial de gas en Virginia](#intoxicaciones-por-pesticidas-en-costa-rica-2007-2014)
  - [Resumen](#resumen)
  - [Estructura del repositorio](#estructura-del-repositorio)
  - [Datos](#datos)
    - [Fuentes de información](#fuentes-de-informaci%C3%B3n)
    - [Descripción del conjuntos de datos](#descripci%C3%B3n-de-los-conjuntos-de-datos)
    - [Variables en el conjunto de datos](#variables-en-cada-conjunto-de-datos)
  - [Procesamiento y análisis de los datos](#procesamiento-y-an%C3%A1lisis-de-los-datos)
    - [Análisis](#an%C3%A1lisis)
  - [Autores](#preguntas)
  - [Licencia](#licencia)

## Estructura del repositorio

El repositorio está compuesto por un archivo de Rmd (R markdown), usado para la limpieza y análisis de los datos, el documento final a entregar en Word, la presentación final en Powerpoint, y una carpeta que contienen los datos usados en el artículo final:

- El archivos de R, disponibles en formato `.Rmd`, contienen los procedimientos usados para la limpieza de los datos y para replicar los resultados y el análisis presentados en el informe final y la presentación (`proyecto3.R`).
- El archivo Word contiene el informe final (`Proyecto 3 - Miguel y Esteban.docx`)
- El archivo Powerpoint contiene la presentación final (`presentacion.pptx`)
- La carpeta `datos` contiene los datos usados en el artículo. 

## Datos

### Fuentes de información

Los datos usados en el análisis y contenidos en la carpeta `datos` provienen de:

- [Geostatistics and Petroleum Geology by M.E. Hohn](http://www.wvgs.wvnet.edu/www/geostat/GeostatPetGeol.html)

### Descripción del conjuntos de datos

Los datos provienen del Sistema de Datos de Petróleo y Gas de la Encuesta Geológica y Económica del oeste de Virginia y son sobre flujos abiertos finales de gas de las rocas del Alto Devónico en un campo en Virginia Occidental con valores del potencial inicial medidos en mil pies cúbicos por día (Mcfpd)

### Variables en el conjunto de datos

1) `appa.xlsx`:

   - **x:** coordenadas de Universal Transverse Mercator (UTM) para la zona 17 UTM hacia el este en kilometros.
   - **y:** coordenadas de Universal Transverse Mercator (UTM) para la zona 17 UTM hacia el norte en kilometros.
   - **pot:** potencial inicial medida en mil pies cúbicos por día (Mcfpd)
  

## Procesamiento y análisis de los datos

Los datos fueron procesados usando R. Se realizó una exploración y transformación de los datos en metros UTM para poder ser utilizado en el formato usual de proyección de los paquetes utlizados para analisis espacial y geoestadística. Teniendo este conjunto de datos en el formato deseado, se realizaron distintos análisis de los datos en R, descritos más a profunidad en el script respectivo y el artículo, que producen, entre otros, los resultados disponibles en el archivo `proyecto3.Rmd`.


### Análisis

Con datos del Sistema de Datos de Petróleo y Gas de la Encuesta Geológica y Económica del oeste de Virginia sobre flujos abiertos finales de gas de las rocas del Alto Devónico en un campo en Virginia Occidental con valores del potencial inicial medidos en mil pies cúbicos por día (Mcfpd) se realizó un análisis univariado utilizando análisis exploratorio y métodos geoestadísticos clásicos como el calculo de semivariograma y modelado del mismo así como estimaciones y mapeo sobre el área usando técnicas de kriging con el fin de determinar el patrón espacial de la variable de interés, la mejor representación gráfica de la continuidad de la variable y cuál es el grado de incertidumbre de estas estimaciones. Los principales resultados arrojan que el mejor método de estimación para semivariograma fue el esférico y que si bien al rededor de donde habían mas puntos muestreados se consiguieron buenas estimaciones con variancia bastante baja, el pobre muestreo del área resultó en correlaciones espaciales bajas en un gran zona con la implicación de alta variabilidad y estimaciones muy cercanas a la media. 


## Autores

- Miguel Coto: cott527@gmail.com
- Esteban Vargas: esvapa8@gmail.com

## Licencia

El código usado y presentado en este repositorio tiene una licencia [MIT](https://opensource.org/licenses/MIT), mientras que los datos y figuras tienen una licencia [CC-BY](https://creativecommons.org/licenses/by/4.0/deed.es), a menos que se especifique explicitamente otra licencia. Las condiciones de las licencias anteriormente mencionadas están descritas en el archivo `LICENSE` de este repositorio.

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Licencia Creative Commons" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Esta obra está bajo una <a rel="license" href="http://creativecommons.org/licenses/by/4.0/deed.es">Licencia Creative Commons Atribución 4.0 Internacional</a>.
