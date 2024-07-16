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
[![Captura-de-pantalla-44.png](https://i.postimg.cc/T3KnrZ0c/Captura-de-pantalla-44.png)](https://postimg.cc/dhK7FNz7)

Para esta etapa se realizo un primer análisis de los datos utilizando la librería de Python Matplotlib para los gráficos y Pandas para trabajar con la data, obteniendo los siguientes resultados:

- Valores faltantes: se encontraron solo 6 valores en la columna **OTROS** de la tabla Accesos por Velocidad.

- Valores Duplicados: No se encontraron duplicados.

- Valores Atipicos (Outliers): en el análisis de los gráficos de disperción se puede ver como Buenos Aires consentra la consentra la mayoria de los Outliers   junto con Capital Federal. Esto no es de sorprender devido a la dencidad poblacional de ambas.Por otro lado en la tabla Ingresos, se puede ver como los ultimos años tienen ingresos cada ves mayores de forma muy escalada, pero que se deve tener en cuenta un factor muy inmportante que es la inflación   de   cada año.

## Conclusiones y Recomendaciones:

Como primera observación podemos ver que las provincias con mayores accesos por tipos de tecnoogía, en el año 2023 son: Buenso Aires, Capital Federal, Cordoba y Santa fe.
[![Captura-de-pantalla-45.png](https://i.postimg.cc/d01mFnHq/Captura-de-pantalla-45.png)](https://postimg.cc/bZ72H0fM)
Al mismo tiempo podemos notar como los accesos por tecnología disminuyen drasticamente en el resto de las provincia. Igual no se tiene que ignorar el hecho de que todas las provincias, con un poco de variación, an tenido un cresimiento constante a traves de los años.
El mismo patron se puede ver en el caso de los accesos por velocidad en el siguiente gráfico.
[![Captura-de-pantalla-46.png](https://i.postimg.cc/DfXVFPHd/Captura-de-pantalla-46.png)](https://postimg.cc/Hjdv9XpV)

