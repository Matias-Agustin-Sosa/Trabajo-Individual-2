# PROYECTO INDIVIDUAL Nº2

## Introducción:
Para este proyecto se recibió un archivo excel con 15 tablas, de las cuales se seleccionaron 6: Accesos por Tecnología, Accesos por Velocidad, Ingresos, Penetración por Hogares, Penetración por Población y Velocidad % por Provincia.
Las mismas poseen informacion del servicio de internet en Argentina provenientes del Ente Nacional de Comunicaciones (ENACOM).

## ETL
[![Captura-de-pantalla-41.png](https://i.postimg.cc/SxBWSg4N/Captura-de-pantalla-41.png)](https://postimg.cc/qNGtQXg9)

En este caso use LibreOffice para la extracción y conversión de las tablas a CSV, ademas de aplicar algunos cambios y transformaciones a los datos, algunas de ellas son:
- Corrección de numeros del alfabeto  español al inglés remplazando comas por puntos en los decimales y quitando los separadores de miles.
- Corregir errores de tipeo (como datos cargados para el cuarto trimestre del 2024 que en realidad es el 4 trimestre del 2023)
- Limpiar comentarios y asteriscos presentes al final de algunas tablas

## EDA


Para esta etapa se realizo un primer análisis de los datos utilizando la librería de Python Matplotlib para los gráficos y Pandas para trabajar con la data, obteniendo los siguientes resultados:

- Valores faltantes: se encontraron solo 6 valores en la columna **OTROS** de la tabla Accesos por Velocidad.

- Valores Duplicados: No se encontraron duplicados.

- Valores Atipicos (Outliers): en el análisis de los gráficos de disperción se puede ver como Buenos Aires consentra la consentra la mayoria de los Outliers   junto con Capital Federal. Esto no es de sorprender devido a la dencidad poblacional de ambas.Por otro lado en la tabla Ingresos, se puede ver como los      ultimos años tienen ingresos cada ves mayores de forma muy escalada, pero que se deve tener en   cuenta un factor muy inmportante que es la inflación   de   cada año.

## Conclusiones y Recomendaciones
