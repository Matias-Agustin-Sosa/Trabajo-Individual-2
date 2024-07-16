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

Lo vemos en el gráfico:

[![Captura-de-pantalla-49.png](https://i.postimg.cc/d3ND2PPX/Captura-de-pantalla-49.png)](https://postimg.cc/4HtJG03b)


## Conclusiones y Recomendaciones:

Como primera observación podemos ver que las provincias con mayores accesos por tipos de tecnoogía, en el año 2023 son: Buenso Aires, Capital Federal, Cordoba y Santa fe.

[![Captura-de-pantalla-45.png](https://i.postimg.cc/d01mFnHq/Captura-de-pantalla-45.png)](https://postimg.cc/bZ72H0fM)

Al mismo tiempo podemos notar como los accesos por tecnología disminuyen drasticamente en el resto de las provincia. Igual no se tiene que ignorar el hecho de que todas las provincias, con un poco de variación, an tenido un cresimiento constante a traves de los años.

El mismo patron se puede ver en el caso de los accesos por velocidad en el siguiente gráfico:

[![Captura-de-pantalla-46.png](https://i.postimg.cc/DfXVFPHd/Captura-de-pantalla-46.png)](https://postimg.cc/Hjdv9XpV)

Por otro lado se puede ver que respecto a los tipos de acceso (Cable Modem, ADSL, Fibra Óptica y Wireless), el más predominante en el año 2023 a sido el Cable Modem.

[![Captura-de-pantalla-47.png](https://i.postimg.cc/631BS67W/Captura-de-pantalla-47.png)](https://postimg.cc/S2C0Yh73)

Devido a esto se planteo el desarrollo de un KPI que aumente la cantidad de Fibra Óptica 7% por Trimestre, un 4% más que los años anteriores aproximadamente. Esto con el fin de brindar un servicio más estable y moderno en temas de conectividad.

Con respecto a los tipos de planes (512 kbps, + 512 Kbps - 1 Mbps, + 1 Mbps - 6 Mbps, etc.), el plan de + 30 Mbps es el que más accesos tiene prcente y que empeso a crecer de gran manera desde 2021 hasta 2023. Lo vemos en el gráfico:

[![Captura-de-pantalla-48.png](https://i.postimg.cc/PqfsjL8W/Captura-de-pantalla-48.png)](https://postimg.cc/v4KS7ZhT)

Viendo esto se plantea el siguiente KPI que propone un seguir aumentando los accesos de + 30 Mbps, esto pude traer mayores ganancias al ser un cervicio mas costoso y muy solicitado devido el avance de la tecnologia y su mayor consumo de Mbps.





