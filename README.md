# PROYECTO INDIVIDUAL Nº2

## Introducción:
Para este proyecto se recibió un archivo Excel con 15 tablas, de las cuales se seleccionaron 6: Accesos por Tecnología, Accesos por Velocidad, Ingresos, Penetración por Hogares, Penetración por Población y Velocidad % por Provincia.
Las mismas poseen informacion del servicio de internet en Argentina provenientes del Ente Nacional de Comunicaciones (ENACOM).

## ETL
[![Captura-de-pantalla-41.png](https://i.postimg.cc/SxBWSg4N/Captura-de-pantalla-41.png)](https://postimg.cc/qNGtQXg9)

En este caso usé LibreOffice para la extracción y conversión de las tablas a CSV, ademas de aplicar algunos cambios y transformaciones a los datos, algunas de ellas son:
- Corrección de números del alfabeto español al inglés reemplazando comas por puntos en los decimales y quitando los separadores de miles.
- Corrección de errores de tipeo (como datos cargados para el cuarto trimestre del 2024 que en realidad es el 4 trimestre del 2023).
- Limpieza de comentarios y asteriscos presentes al final de algunas tablas.

## EDA
[![Captura-de-pantalla-44.png](https://i.postimg.cc/T3KnrZ0c/Captura-de-pantalla-44.png)](https://postimg.cc/dhK7FNz7)

Para esta etapa se realizó un primer análisis de los datos utilizando la librería de Python Matplotlib para los gráficos y Pandas para trabajar con la data, obteniendo los siguientes resultados:

- Valores faltantes: se encontraron solo 6 valores en la columna **OTROS** de la tabla Accesos por Velocidad.

- Valores Duplicados: No se encontraron duplicados.

- Valores Atipicos (Outliers): en el análisis de los gráficos de dispersión se puede ver como Buenos Aires concentra la mayoría de los Outliers junto con Capital Federal. Esto no es raro debido a la densidad poblacional de ambas. Por otro lado en la tabla Ingresos, se puede ver como los últimos años tienen ingresos cada vez mayores de forma muy escalada, aunque se debe tener en cuenta un factor muy importante que es la inflación de cada año.

Lo vemos en el gráfico:

[![Captura-de-pantalla-49.png](https://i.postimg.cc/d3ND2PPX/Captura-de-pantalla-49.png)](https://postimg.cc/4HtJG03b)


## Conclusiones y Recomendaciones:

Como primera observación podemos ver que las provincias con mayores accesos por tipos de tecnología, en el año 2023 son: Buenso Aires, Capital Federal, Córdoba y Santa Fe.

[![Captura-de-pantalla-45.png](https://i.postimg.cc/d01mFnHq/Captura-de-pantalla-45.png)](https://postimg.cc/bZ72H0fM)

Al mismo tiempo podemos notar como los accesos por tecnología disminuyen drásticamente en el resto de las provincia. Igual no se tiene que ignorar el hecho de que todas las provincias, con un poco de variación, han tenido un crecimiento constante a través de los años.

El mismo patron se puede ver en el caso de los accesos por velocidad en el siguiente gráfico:

[![Captura-de-pantalla-46.png](https://i.postimg.cc/DfXVFPHd/Captura-de-pantalla-46.png)](https://postimg.cc/Hjdv9XpV)

Por otro lado se puede ver que respecto a los tipos de acceso (Cable Modem, ADSL, Fibra Óptica y Wireless), el más predominante en el año 2023 ha sido el Cable Modem.

[![Captura-de-pantalla-47.png](https://i.postimg.cc/631BS67W/Captura-de-pantalla-47.png)](https://postimg.cc/S2C0Yh73)

Debido a esto se planteó el desarrollo de un KPI que aumente la cantidad de accesos de Fibra Óptica un 7% por Trimestre, un 4% más que los años anteriores aproximadamente. Esto con el fin de brindar un servicio más estable y moderno en temas de conectividad.

Con respecto a los tipos de planes (512 kbps, + 512 Kbps - 1 Mbps, + 1 Mbps - 6 Mbps, etc.), el plan de + 30 Mbps es el que más accesos tiene y que empezó a crecer de gran manera desde 2021 hasta 2023. Lo vemos en el gráfico:

[![Captura-de-pantalla-48.png](https://i.postimg.cc/PqfsjL8W/Captura-de-pantalla-48.png)](https://postimg.cc/v4KS7ZhT)

Viendo esto se planteó el siguiente KPI que propone seguir aumentando los accesos de + 30 Mbps un 3% por trimestre, un 1% más que el año anterior, con el fin de aumentar las ganancias por ser un servicio de los más costosos y muy solicitado debido al avance de la tecnología y su mayor consumo de Mbps.

Por otro lado, si vemos la penetración por hogares y población, en el año 2023, podemos ver que los gráficos son más parejos y con decrecimientos más controlados:

[![Captura-de-pantalla-53.png](https://i.postimg.cc/c4KfFT9Y/Captura-de-pantalla-53.png)](https://postimg.cc/kBmV4NdX)

[![Captura-de-pantalla-54.png](https://i.postimg.cc/85KrHrLt/Captura-de-pantalla-54.png)](https://postimg.cc/G8D23t7y)

Esto refleja que el alcance del producto, por habitantes y hogares, en cada provincia es bueno.
Además, se calculó el KPI propuesto que pedía aumentar un 2% por trimestre los nuevos accesos por cada 100 hogares.

Para concluir también podemos observar el promedio de velocidad porcentual por provincia en el año 2023. Se ve claramente la predominancia de Capital federal, pero también la similitud entre el resto de las provincias exceptuando algunas como: La Pampa, San Juan, Santa Cruz, Chubut y Tierra del Fuego. En el caso de las provincias patagonicas es de esperar debido a las largas distancias entre ciudades y las bajas poblaciones en ellas, lo que aumenta el costo de servicio.

[![Captura-de-pantalla-52.png](https://i.postimg.cc/D04mPpvw/Captura-de-pantalla-52.png)](https://postimg.cc/LgRHHTgc)
