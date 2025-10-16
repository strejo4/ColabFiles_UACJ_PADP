# ColabFiles_UACJ_PADP
Este repositorio contiene las prácticas del curso de Programación para Analítica Descriptiva y Predictiva.

## Practica 1 
En esta practica, el codigo analiza el archivo mbox.txt y extrae las mediciones que contienen la cadena X-DSPAM-Confidence, calculando:
- Cantidad de datos extraidos
- Sumatoria de los datos
- Promedio de los datos
- Varianza de los datos

Como obtuve los resultados:
1. Abri el archivo mbox.txt en Python usando open().
2. Recorri cada linea con un bucle for.
3. Filtre las lineas que contienen X-DSPAM-Confidence.
4. Extraje el valor numerico despues de los dos puntos : y lo converti a float.
5. Guarde todos los valores en una lista.
6. Calcule cantidad, sumatoria, promedio y varianza con funciones de Python y NumPy.
7. Mostre los resultados en pantalla con print().

Para reproducir los resultados:
1. Abrir Practica1_SergioTrejo.ipynb en Google Colab o Jupyter Notebook.
2. Ejecutar las celdas en orden.

Para reproducir los resultados:
1. Abrir Practica1_SergioTrejo.ipynb en Google Colab o Jupyter Notebook.
2. Ejecutar las celdas en orden.

## Práctica 2
En esta practica, el codigo analiza el archivo informe_acciones.txt en dos partes:

1. Lectura del archivo (demostracion):  
   - Abri el archivo informe_acciones.txt en Python usando open() con codificacion latin-1.
   - Se muestran solamente las primeras 150 lineas para visualizar el contenido sin imprimir todo el archivo.

2. Analisis de datos (practica principal):  
   - Extrae el nombre y ticker de cada empresa.
   - Obtiene las fechas registradas de las mediciones.
   - Obtiene los valores actuales de las acciones.
   - Calcula para cada empresa:
     - Fecha mas reciente.
     - Valor maximo.
     - Valor minimo.
     - Promedio de los valores.

Como se obtuvieron los resultados:
1. Abri el archivo informe_acciones.txt en Python usando open() con codificacion latin-1.
2 Recorri cada linea del archivo con un bucle for.
3. Use expresiones regulares re.findall() para:
   - Encontrar "accion de" y extraer nombre y ticker.
   - Encontrar "Fecha:" y guardar la fecha.
   - Encontrar "Valor actual:" y guardar el valor como float.
4. Se guardo la informacion en un diccionario, usando el nombre y ticker como clave, y listas para almacenar las fechas y valores.
5. Se calcularon para cada empresa la fecha mas reciente, el valor maximo, el valor minimo y el promedio.
6. Se mostros los resultados en una tabla alineada usando f-strings con formato de columnas.

Para reproducir los resultados:
1. Abrir Practica2_SergioTrejo.ipynb en Google Colab o Jupyter Notebook.

## Practica 3
En esta practica se estan creando un arregloo en NumPy y se realizan operaciones basicas:
- Arreglo de 20 numeros aleatorios entre 1 y 100.
- Calculo de maximo, minimo y media.
- Suma de 10 a cada elemento.

Como se obtuvierons los resultados:
1. Se importo NumPy y se genero el arreglo con np.random.randint().
2. Calculos de maximo, minimo y media con np.max(), np.min() y np.mean().
3. Se sumo 10 al arreglo usando operaciones vectorizadas.
4. Los resultados se mostraron con print() en cada operacion. 

Para reproducir los resultados:
1. Abrir Practica3_SergioTrejo.ipynb en Google Colab o Jupyter Notebook.
2. Ejecutar las celdas en orden.

## Practica 4
En esta practica se trabajan operaciones con matrices en NumPy:
- Crear dos matrices 3x3 con numeros aleatorios entre 1 y 10.
- Sumar las dos matrices.
- Restar la segunda matriz de la primera.
- Multiplicar la primera matriz por 2.
- Realizar multiplicacion matricial entre ambas.

Como se obtuvieron los resultados:
1. Se importo NumPy y genere dos matrices con np.random.randint().
2. Se utilizaron operadores (+, -, *) y la funcion np.dot() para las operaciones.
3. Los resultados se mostraron con print().

Para reproducir los resultados:
1. Abrir Practica4_SergioTrejo.ipynb en Google Colab o Jupyter Notebook.
2. Ejecutar las celdas en orden.

## Practica 5
En esta practica se utilizan mascaras booleanas en NumPy:
- Crear un arreglo de 15 numeros aleatorios entre 1 y 50.
- Seleccionar los elementos mayores que 25 usando una mascara booleana.
- Contar cuantos elementos son mayores que 25.

Como se obtuvieron los resultados:
1. Se importo NumPy y se genero un arreglo con np.random.randint().
2. Se creo una mascara booleana con la condicion arreglo > 25.
3. Se filtraron los elementos usando arreglo[mask].
4. Se conto la cantidad de elementos mayores que 25 con np.sum(mask).
5. Los resultados se mostraron con print().

Para reproducir los resultados:
1. Abrir Practica5_SergioTrejo.ipynb en Google Colab o Jupyter Notebook.
2. Ejecutar las celdas en orden.

## Practica 6

En esta practica se utiliza la libreria Pandas y NUmpY para analizar el dataset Titanic. Se desarrollan 5 ejercicios:

1. Calcular la proporcion de supervivencia para cada combinacion de 'Sex' y 'Pclass', identificando la combinacion con mayor y menor tasa de supervivencia.
2. Crear una columna 'FamilySize' sumando 'Siblings/Spouses Aboard' y 'Parents/Children Aboard'. Identificar familias grandes (FamilySize > 3), calcular el numero de pasajeros en familias grandes y la proporcion de supervivencia en este grupo.
3. Segmentar a los pasajeros en dos grupos de edad mediante una funcion: 'Menor de Edad' (<18) y 'Mayor de Edad' (>=18).
4. Calcular el promedio de las columnas 'Age' y 'Fare' de dos formas: manualmente con NumPy (limpiando valores NaN) y con Pandas (mean() ignora NaN por defecto). Verificar la consistencia entre ambos resultados.
5. Crear intervalos equidistantes para 'Fare' usando np.linspace y asignar a cada pasajero el intervalo correspondiente mediante pd.cut. Calcular el numero de pasajeros en cada intervalo y la proporcion de supervivencia por intervalo.

Como se obtuvieron los resultados:
1. Se importo el dataset Titanic con Pandas y se trabajo sobre las columnas 'Survived', 'Pclass', 'Sex', 'Age', 'Fare', 'Siblings/Spouses Aboard' y 'Parents/Children Aboard'.
2. Se aplicaron funciones de agrupamiento (groupby), filtrado con mascaras booleanas, creacion de nuevas columnas con operaciones aritmeticas y funciones definidas por el usuario.
3. Se utilizaron funciones de NumPy como np.linspace y limpieza de NaN con np.isnan() para los calculos manuales.
4. Se usaron metodos nativos de Pandas como mean(), value_counts(), groupby() y cut() para obtener resultados de forma directa.
5. Los resultados se imprimieron en pantalla con print().

Para reproducir los resultados:
1. Abrir Practica6_SergioTrejo.ipynb en Google Colab o Jupyter Notebook.
2. Ejecutar las celdas en orden.

## Practica 7 

En esta practica se utiliza la libreria Matplotlib junto con el dataset Iris de seaborn para visualizar datos. Se desarrollaron 6 actividades:

1. Cargar el dataset Iris con sns.load_dataset('iris'), revisar las primeras filas con .head() y obtener informacion general de las columnas.
2. Crear un grafico de barras para comparar los promedios de petal_length y petal_width entre las tres especies de Iris.
3. Elaborar un histograma de sepal_length para observar la distribucion de los largos de los sepalos.
4. Realizar un grafico de dispersion (scatter plot) relacionando petal_length y petal_width, asignando un color distinto a cada especie.
5. Constrir graficos de cajas (box plots) para mostrar la distribucion de sepal_length y sepal_width por especie, detectando diferencias y posibles outliers en los datos.
6. Generar un grafico de lineas para visualizar la tendencia de petal_length a lo largo de las observaciones.

Como se obtuvieron los resultados:
1. Se importo el dataset Iris desde seaborn (sns.load_dataset) y se trabajo sobre las columnas sepal_length, sepal_width, petal_length, petal_width y species.
2. Se calcularon promedios y se aplicaron tecnicas de agrupamiento con groupby para resumir datos por especie.
3. Se generaron diferentes graficos con Matplotlib (bar, hist, scatter, boxplot, plot) para representar los datos.
4. Se usaron parametros visuales como alpha (transparencia de datos), cmap (mapa de colores) y etiquetas (xlabel, ylabel, title) para mejorar la interpretacion de los datos.
5. Los resultados se imprimieron en pantalla utilizando plt.show().

Para reproducir los resultados:
1. Abrir Practica7_SergioTrejo.ipynb en Google Colab o Jupyter Notebook.
2. Ejecutar las celdas en orden.

##Practica 8

En esta practica se utiliza la libreria Seaborn junto con el dataset tips para visualizar datos. Se desarrollaron 3 actividades:

1. Cargar el dataset tips con sns.load_dataset('tips'), revisar las primeras filas con .head(), obtener informacion general de las columnas con .info() y .describe(), y verificar si existen valores nulos.
2. Elaborar un mapa de calor (heatmap) mostrando la correlacion entre las variables numericas total_bill, tip y size. Personalizar el grafico con anotaciones y una paleta de colores.
3. Construir un diagrama de violin para mostrar la distribucion de las propinas (tip) por dia de la semana, observando la variabilidad y forma de la distribucion.
4. Generar un grafico de dispersion (scatter plot) para analizar la relacion entre total_bill y tip, asignando colores diferentes a cada dia de la semana.

Como se obtuvieron los resultados:
1. Se importo el dataset tips desde seaborn (sns.load_dataset).
2. Se realizo un analisis exploratorio con metodos como head(), info() y describe() para conocer la estructura de los datos.
3. Se calculo la correlacion entre variables numericas con corr() y se represento en un mapa de calor usando sns.heatmap con parametros como annot y cmap.
4. Se utilizo sns.violinplot para graficar la distribucion de tip por dia, mostrando la densidad y variabilidad de los datos.
5. Se empleo sns.scatterplot para representar la relacion entre total_bill y tip, utilizando un mapa de colores para diferenciar los dias de la semana.
6. Los resultados se imprimieron en pantalla utilizando plt.show().

Para reproducir los resultados:
1. Abrir Practica8_SergioTrejo.ipynb en Google Colab o Jupyter Notebook.
2. Ejecutar las celdas en orden.

## Practica 9 

En esta practica se utiliza la libreria Plotly Express junto con el dataset gapminder para visualizar datos. 
Se desarrollaron las siguientes actividades:

1. Cargar el dataset gapminder con px.data.gapminder(), revisar las primeras filas con .head(), obtener informacion general de las columnas y verificar su estructura.
2. Filtrar el dataset para el año 2007, de modo que solo se incluyan los registros correspondientes a ese año.
3. Construir un grafico de dispersion (scatter plot) donde el eje X representa el gdpPercap y el eje Y la esperanza de vida (lifeExp).
4. Personalizar el grafico asignando el tamano de los puntos segun la poblacion (pop) y el color segun el continente.

Para reproducir los resultados:
1. Abrir Practica9_SergioTrejo.ipynb en Google Colab o Jupyter Notebook.
2. Ejecutar las celdas en orden.

## Practica 10

En esta practica se utiliza la libreria Plotly Express junto con el dataset tips de seaborn para visualizar datos. 
Se desarrollaron las siguientes actividades:

1. Cargar el dataset tips usando sns.load_dataset("tips"), revisar las primeras filas con .head(), y verificar su estructura.
2. Generar un histograma de la variable tip usando plotly.express.histogram().
3. Personalizar el numero de bins para ajustar el nivel de detalle de la distribucion.
4. Asignar colores a las barras segun la variable dia de la semana para observar diferencias entre dias.
5. Ajustar la separacion entre barras mediante el parametro bargap para mejorar la visualizacion.
6. Agregar etiquetas y un titulo descriptivo a la grafica.

Como se obtuvieron los resultados:
1. Se importaron las librerias seaborn y plotly.express.
2. Se cargo el dataset tips desde seaborn y se reviso su contenido.
3. Se utilizo la funcion px.histogram() para graficar la distribucion de tip.
4. Se agregaron parametros como nbins para el numero de intervalos, color="day" para diferenciar por dia, y labels para renombrar las variables.
5. Se personalizo el layout de la grafica con fig.update_layout(bargap=0.2).
6. Los resultados se visualizaron directamente en Google Colab mediante fig.show().

Para reproducir los resultados:
1. Abrir Practica10_SergioTrejo.ipynb en Google Colab o Jupyter Notebook.
2. Ejecutar las celdas en orden.

## Practica 11

En esta practica se utiliza Plotly para graficar series de tiempo de precios de acciones usando el dataset stocks incluido en plotly.express.
Se desarrollaron las siguientes actividades:

1. Cargar el dataset stocks con px.data.stocks() y revisar las primeras filas con .head().
2. Crear un grafico de lineas donde el eje X es la fecha (date) y el eje Y el precio de cierre de cada empresa.
3. Agregar una traza (linea) por empresa usando plotly.graph_objects (go.Scatter) dentro de un ciclo for.
4. Diferenciar cada compania con colores: Plotly asigna colores automaticamente a cada traza.
5. Personalizar titulos y etiquetas de ejes.

Como se obtuvieron los resultados:
1. Se importaron las librerias necesarias: plotly.express como px y plotly.graph_objects como go.
2. Se cargo el dataset con df = px.data.stocks().
3. Se creo una figura vacia con fig = go.Figure().
4. Se recorrio la lista de empresas con for company in df.columns[1:]: 
   Se agrego cada linea con fig.add_trace(go.Scatter(x=df['date'], y=df[company], mode='lines', name=company)).
5. Se ajusto el layout de la grafica con:
   fig.update_layout(title="Evolucion del precio de acciones", xaxis_title="Fecha", yaxis_title="Precio de cierre").
6. Se visualizo el resultado con fig.show().

Para reproducir los resultados:
1. Abrir Practica11_SergioTrejo.ipynb en Google Colab o Jupyter Notebook.
2. Ejecutar las celdas en orden.

## Practica 12

En esta practica se utiliza la libreria Plotly Graph Objects junto con el dataset flights de seaborn para crear un mapa de calor.
Se desarrollaron las siguientes actividades:

1. Cargar el dataset flights usando sns.load_dataset("flights") y revisar las primeras filas con .head().
2. Reorganizar los datos con pivot para que los años aparezcan como filas, los meses como columnas y los valores de pasajeros en las celdas:
   datos_transformados = df.pivot(index='year', columns='month', values='passengers')
3. Crear un mapa de calor con go.Heatmap usando los valores de la tabla pivotada:
   - z = datos_transformados.values (valores de pasajeros)
   - x = datos_transformados.columns (meses)
   - y = datos_transformados.index (años)
4. Mostrar el grafico interactivo con fig.show().

Como se obtuvieron los resultados:
1. Se importaron seaborn y plotly.graph_objects.
2. Se cargo el dataset flights y se transformo con pivot para reoorganizarlo.
3. Se construyo el heatmap con go.Figure(data=go.Heatmap(...)).
4. Se agregaron titulo y etiquetas a los ejes con fig.update_layout().
5. El resultado se visualizo de forma interactiva.

Para reproducir los resultados:
1. Abrir Practica12_SergioTrejo.ipynb en Google Colab o Jupyter Notebook.
2. Ejecutar las celdas en orden.

## Practicas 13 

En estas practicas se utilizo la libreria pandas para realizar operaciones de carga, limpieza, normalizacion y verificacion de tipos de datos sobre el dataset miaad-nyc-r-s.csv.

Se desarrollaron las siguientes actividades:

Carga de Datos
1. Se cargo el archivo CSV omitiendo la ultima linea irrelevante ("Esta es una linea que no deberias cargar").
2. Se utilizo df.tail(3) para comprobar que no se cargo la linea basura.
3. Se imprimieron las dimensiones del dataframe con df.shape.

 Agregar una Columna
1. Se imprimieron los nombres originales de las columnas.
2. Se verifico que la primera columna tuviera el nombre INDEX MIIAD.
3. Como aparecia como Unnamed: 0, se renombro correctamente a INDEX MIIAD.
4. Se volvio a imprimir la lista de columnas para confirmar el cambio.

 Normalizacion de Columnas
1. Se normalizaron los nombres de las columnas para que estuvieran en minusculas y los espacios se reemplazaran con guion bajo "_".
2. Ejemplo: "SALE PRICE" -> "sale_price".
3. Se imprimieron los nombres de las columnas despues de la normalizacion.

Errores en los Tipos de Datos
1. Se imprimieron los tipos de datos de todas las columnas.
2. Se detecto que las columnas sale_price, land_square_feet y gross_square_feet estaban en tipo object.
3. Se convirtieron explicitamente a tipo float64 usando:
   pd.to_numeric(df['columna'], errors='coerce').astype('float64')
4. Se imprimieron nuevamente los tipos de datos para demostrar la correccion.

Diccionario de Datos
1. Se genero un diccionario de datos utilizando df.dtypes.to_dict().
2. Se imprimio mostrando cada columna con su tipo de dato.

Como se obtuvieron los resultados:
1. Se utilizo la libreria pandas.
2. Se cargo el dataset con pd.read_csv() usando el parametro skipfooter=1 para eliminar la linea basura al final. 
3. Se aplicaron metodos como df.rename(), df.columns.str.lower(), pd.to_numeric(), y df.astype().
4. Se genero un diccionario de datos con df.dtypes.to_dict().

Para reproducir los resultados:
1. Abrir el archivo Practica13_SergioTrejo.ipynb en Google Colab o Jupyter Notebook.
2. Ejecutar las celdas en orden.

## Practicas 14

En esta practica se utiliza la libreria pandas junto con el dataset nls97.csv para realizar operaciones de limpieza y transformacion de datos categoricos.
Se desarrollaron las siguientes actividades:

1. Imprimir los valores unicos de la columna maritalstatus con .unique() y su frecuencia con .value_counts().
2. Reemplazar el valor Never-married por Single utilizando .replace() y verificar los cambios con .value_counts().
3. Imprimir los valores unicos de la columna highestdegree con .unique() y su frecuencia con .value_counts().
4. Quitar el numero inicial en cada categoria de highestdegree usando .str.replace() y convertir los valores a minusculas con .str.lower().
   Ejemplo: "2. High School" -> "high school".
5. Agrupar las categorias Widowed y Single en una nueva categoria llamada Single/No Partner usando .replace().
   - Se creo una nueva columna maritalstatus_grouped.
   - Se imprimieron los valores unicos con .unique() y las frecuencias con .value_counts().
6. Imprimir el tipo de dato de la columna gender con .dtype y la memoria ocupada con .memory_usage(deep=True).
7. Convertir la columna gender de object a category con .astype('category') y volver a imprimir el tipo de dato y la memoria ocupada.

Como se obtuvieron los resultados:
1. Se importo la libreria pandas.
2. Se cargo el dataset nls97.csv en un DataFrame con pd.read_csv().
3. Se utilizaron metodos de pandas para limpieza de valores y estandarizacion de categorias (.unique, .value_counts, .replace, .str.replace, .str.lower).
4. Se agruparon categorias de baja frecuencia en una nueva categoria general.
5. Se transformaron tipos de datos object a category con .astype para optimizar el uso de memoria.

Para reproducir los resultados:
1. Abrir Practica14_SergioTrejo.ipynb en Google Colab o Jupyter Notebook.
2. Subir el archivo nls97.csv a la ruta correspondiente en Google Drive.
3. Ejecutar las celdas en orden.

## Practica 15

En esta practica se utiliza la libreria pandas junto con el dataset Airdata.csv para realizar operaciones con datos de tipo fecha y tiempo.  
Se desarrollaron las siguientes actividades:

1. Verificar que las columnas tengan el tipo de datos correcto usando dtypes.
   - Se convirtio la columna DateTime a tipo datetime64 con pd.to_datetime().
   - Se imprimieron los tipos de datos despues de la conversion y las primeras 3 lineas del dataset.

2. Extraer componentes de la columna DateTime.
   - Se crearon nuevas columnas Year, Month, Day y Hour.
   - Se imprimieron las primeras filas del dataframe para verificar los cambios.

3. Realizar operaciones aritmeticas con fechas usando timedelta.
   - Se definio un intervalo de 10 dias, 7 horas y 15 minutos con datetime.timedelta.
   - Se sumo el intervalo a la columna DateTime y se guardo en una nueva columna DateTime_Suma.
   - Se imprimieron las columnas DateTime y DateTime_Suma.

4. Convertir la columna DateTime a formato Unix timestamp.
   - Se recorrio la columna DateTime con un ciclo for y se aplico .timestamp() a cada valor.
   - Se guardaron los resultados en una lista y despues en una nueva columna DateTime_Unix.
   - Se imprimieron las columnas DateTime y DateTime_Unix, mostrando las primeras 3 lineas.

5. Filtrar datos a partir de la columna DateTime.
   - Se seleccionaron las filas con fechas mayores a 2020-11-01.
   - Se imprimio el resultado.

Como se obtuvieron los resultados:
1. Se importo la libreria pandas y datetime.
2. Se cargo el dataset Airdata.csv en un DataFrame con pd.read_csv().
3. Se convirtio la columna DateTime de tipo object a datetime con pd.to_datetime().
4. Se extrajeron componentes de fecha y hora con .dt.year, .dt.month, .dt.day, .dt.hour.
5. Se realizaron operaciones de aritmetica de fechas con datetime.timedelta.
6. Se transformo la columna DateTime a formato Unix timestamp con .timestamp() usando un ciclo for.
7. Se aplico un filtro sobre la columna DateTime para seleccionar fechas mayores a 2020-11-01.

Para reproducir los resultados:
1. Abrir Practica15_SergioTrejo.ipynb en Google Colab o Jupyter Notebook.
2. Subir el archivo Airdata.csv a la ruta correspondiente en Google Drive.
3. Ejecutar las celdas en orden.

## Practica 16 

En esta practica se utiliza la libreria pandas junto con el dataset dirtydata.csv para realizar operaciones de limpieza relacionadas con valores perdidos y datos duplicados.  

Se desarrollaron las siguientes actividades:

1. Ejercicio 01: Datos perdidos
   - Se cargo el dataset dirtydata.csv y se verifico la carga.
   - Se imprimio la cantidad de datos perdidos en cada columna.
   - Se calculo la media de la columna Calories.
   - Se aplico imputacion por promedio (mean) en la columna Calories.
   - Se recalculo la media de la columna Calories despues de imputar.

2. Ejercicio 02: Duplicidad parcial (una columna)
   - Se identificaron registros duplicados en la columna Duration.
   - Se utilizo value_counts() para obtener la frecuencia de valores unicos en Duration.
   - Se eliminaron los registros duplicados en Duration.

3. Ejercicio 03: Duplicidad parcial (dos columnas)
   - Se identificaron registros duplicados en las columnas Pulse y Maxpulse.
   - Se utilizo value_counts() para obtener la frecuencia de combinaciones unicas en Pulse y Maxpulse.
   - Se eliminaron los duplicados parciales conservando la ultima ocurrencia (keep='last').

4. Ejercicio 04: Duplicidad total o exacta
   - Se contaron los registros duplicados exactos en todas las columnas del dataset.
   - Se utilizo sum() para obtener la cantidad de duplicados exactos.
   - Se eliminaron los duplicados exactos conservando la ultima ocurrencia.

5. Ejercicio 05: Media con y sin duplicados
   - Se calcularon las medias de las columnas Pulse y Maxpulse en el dataset original con duplicados.
   - Se eliminaron los duplicados parciales en Pulse y Maxpulse conservando la ultima ocurrencia.
   - Se recalcularon las medias de Pulse y Maxpulse en el dataset limpio para comparar.

Como se obtuvieron los resultados:
- Se utilizo la libreria pandas.
- Se cargo el dataset dirtydata.csv en un DataFrame con pd.read_csv().
- Se aplicaron metodos de pandas para deteccion y limpieza de datos perdidos y duplicados (.isnull(), .mean()

Para reproducir los resultados:
1. Abrir Practica16_SergioTrejo.ipynb en Google Colab o Jupyter Notebook.
2. Subir el archivo dirtydata.csv a la ruta correspondiente en Google Drive.
3. Ejecutar las celdas en orden.

## Practica 18

En esta practica se utiliza la libreria pandas, matplotlib, seaborn y scipy.stats junto con el dataset AirQuality.csv para realizar un Analisis Exploratorio de Datos (EDA), incluyendo limpieza, tratamiento de datos faltantes, visualizaciones y pruebas de normalidad.  

Se desarrollaron las siguientes actividades:  

1. Cargar el dataset AirQuality.csv con separador ";".  
2. Eliminar las columnas vacias (Unnamed: 15 y Unnamed: 16).  
3. Reemplazar valores -200 por NaN en todo el DataFrame.  
4. Convertir columnas numericas que estaban como texto (CO(GT), C6H6(GT), T, RH, AH) a tipo float64.  
5. Imputar valores faltantes:  
   - Numericos con la media.  
   - Categoricos con la moda.  
6. Obtener la descripcion estadistica del dataset (media, mediana, desviacion estandar, minimos, maximos y percentiles).  
7. Generar histogramas para todas las variables numericas.  
8. Crear graficas de barras para las variables categoricas (Date y Time).  
9. Dibujar boxplots para identificar outliers en variables numericas.  
10. Construir la matriz de correlacion y visualizarla con un heatmap.  
11. Generar un pairplot para observar relaciones entre variables numericas.  
12. Realizar pruebas de normalidad (Shapiro-Wilk, Anderson-Darling y Kolmogorov-Smirnov).  
13. Generar QQplots para confirmar visualmente la normalidad de las distribuciones.  


Como se obtuvieron los resultados:  
1. Se importaron las librerias pandas, numpy, matplotlib, seaborn y scipy.stats.  
2. Se cargo el dataset en un DataFrame usando pd.read_csv().  
3. Se limpiaron los datos reemplazando valores -200 por NaN.  
4. Se transformaron columnas de tipo object a float64.  
5. Se imputaron valores faltantes con media y moda segun el tipo de variable.  
6. Se realizaron analisis estadisticos descriptivos (describe(), median()).  
7. Se generaron graficas (histogramas, barras, boxplots, heatmap, pairplot).  
8. Se aplicaron pruebas de normalidad y se graficaron QQplots.  



Para reproducir los resultados:  
1. Abrir Practica18_SergioTrejo.ipynb en Google Colab o Jupyter Notebook.  
2. Subir el archivo AirQuality.csv a la ruta correspondiente en Google Drive.  
3. Ejecutar las celdas en orden.


## Practica 20  

En esta practica se utilizaron las librerias NumPy, Pandas, Matplotlib, Seaborn y Scipy junto con funciones de scikit-learn para aplicar distintos metodos de normalizacion y transformacion de datos.  

Se desarrollaron las siguientes actividades:  

---

1. Ejercicio 01: Normalizacion Min-Max  
- Se cargo el dataset wine de sklearn y se selecciono la variable alcohol.  
- Se realizo una prueba de normalidad antes de la normalizacion.  
- Se aplico la normalizacion Min-Max Scaling para ajustar los valores al rango [0,1].  
- Se volvio a aplicar la prueba de normalidad.  
- Se graficaron los datos originales y normalizados.  
- Resultado: la escala cambio, pero la forma de la distribucion no se modifico. La normalizacion no afecto la normalidad de los datos.  

---

2. Ejercicio 02: Normalizacion Z-Score  
- Se utilizo la variable malic_acid del dataset wine.  
- Se realizo la prueba de normalidad sobre los datos originales.  
- Se aplico la normalizacion Z-Score, centrando la media en 0 y la desviacion estandar en 1.  
- Se compararon los resultados y las graficas.  
- Resultado: los datos mantuvieron su forma original, pero fueron estandarizados. Esta tecnica es util para comparar variables con diferentes unidades y magnitudes.  

---

3. Ejercicio 03: Transformacion Logaritmica  
- Se genero un conjunto de datos aleatorios positivos con distribucion exponencial.  
- Se aplico la transformacion logaritmica (np.log) para reducir la asimetria.  
- Se evaluo la normalidad antes y despues de la transformacion.  
- Se graficaron ambas distribuciones.  
- Resultado: la transformacion redujo la asimetria y acerco los datos a una distribucion mas normal. Los valores grandes se comprimieron, suavizando la cola derecha.  

---

4. Ejercicio 04: Transformacion Raiz Cuadrada  
- Se generaron datos con distribucion exponencial.  
- Se aplico la transformacion raiz cuadrada (np.sqrt).  
- Se realizaron pruebas de normalidad y comparaciones graficas.  
- Resultado: la raiz cuadrada redujo el sesgo y estabilizo la varianza, disminuyendo el impacto de los valores extremos sin alterar excesivamente la forma de la distribucion.  

---

5. Ejercicio 05: Transformacion Box-Cox  
- Se generaron datos con distribucion exponencial.  
- Se aplico la transformacion Box-Cox (scipy.stats.boxcox) y se obtuvo el valor optimo de lambda (λ).  
- Se compararon las distribuciones antes y despues de la transformacion.  
- Resultado: Box-Cox redujo el sesgo y acerco los datos a una forma mas normal. El valor de lambda indico el tipo de ajuste aplicado:  
  - lambda ≈ 1 -> transformacion lineal  
  - lambda ≈ 0 -> logaritmica  
  - lambda ≈ 0.5 -> raiz cuadrada  
  El metodo selecciono automaticamente el lambda optimo para mejorar la simetria y homogeneidad de los datos.  

---

Como se obtuvieron los resultados:  
- Se aplicaron metodos de escalado y transformacion usando funciones de sklearn.preprocessing y scipy.stats.  
- Se evaluo la normalidad con Shapiro-Wilk (stats.shapiro).  
- Se usaron graficos de dispersion e histogramas con Seaborn y Matplotlib para comparar las distribuciones antes y despues de cada proceso.  

---

Para reproducir los resultados:  
1. Abrir el archivo Practica20_SergioTrejo.ipynb en Google Colab o Jupyter Notebook.  
2. Ejecutar cada bloque de codigo secuencialmente.  
3. Observar las salidas graficas y los resultados de las pruebas estadisticas.  


## Practica 21

En esta practica se utiliza la libreria Scikit-Learn junto con el dataset restaurantes.csv para realizar un modelo de regresion lineal simple, analizando la relacion entre la poblacion de una ciudad y las ganancias promedio de un restaurante.

Se desarrollaron las siguientes actividades:

1. Se importaron las bibliotecas necesarias (pandas, numpy, matplotlib, seaborn, scipy y sklearn).
2. Se cargo el archivo restaurantes.csv y se realizo una descripcion estadistica del conjunto de datos.
3. Se analizaron los posibles valores atipicos mediante boxplots.
4. Se realizo un analisis exploratorio grafico (diagrama de dispersion) para observar la relacion entre poblacion y ganancia.
5. Se calculo el coeficiente de correlacion de Pearson para determinar la fuerza y direccion de la relacion entre las variables.
6. Se construyo un modelo de regresion lineal simple utilizando Scikit-Learn.
7. Se obtuvieron e interpretaron el intercepto y la pendiente del modelo.
8. Se grafico la linea de regresion sobre los datos reales para visualizar el ajuste del modelo.
9. Se calcularon e interpretaron los residuos para verificar los supuestos del modelo (normalidad y homocedasticidad).
10. Se elaboro el grafico Q-Q Plot para evaluar la normalidad de los residuos.
11. Se evaluo el desempeno del modelo utilizando las metricas MSE, RMSE y R2.
12. Finalmente, se redactaron las conclusiones sobre la utilidad, limitaciones y necesidad de estandarizacion de las variables.

---

### Como se obtuvieron los resultados:
- Se importaron las bibliotecas pandas, numpy, seaborn, matplotlib, scipy y sklearn.
- Se cargo el dataset restaurantes.csv desde Google Drive.
- Se aplicaron metodos de analisis exploratorio y visualizacion de datos (histogramas, boxplots, graficos de dispersion).
- Se construyo el modelo de regresion lineal simple y se interpretaron los coeficientes.
- Se verificaron los supuestos del modelo mediante el analisis de residuos y graficos Q-Q.
- Se calcularon las metricas de desempeno (MSE, RMSE y R2).
- Se redactaron las conclusiones con base en los resultados obtenidos.

---

### Para reproducir los resultados:
1. Abrir el archivo Practica21_SergioTrejo.ipynb en Google Colab o Jupyter Notebook.
2. Cargar el archivo restaurantes.csv en la ruta correspondiente.
3. Ejecutar todas las celdas en orden.


## Practica 22

En esta practica se utiliza la libreria Scikit-Learn junto con el dataset advertising.csv para realizar un modelo de regresion lineal multiple, analizando la relacion entre las inversiones publicitarias (TV, Radio y Newspaper) y las ventas del producto.

Se desarrollaron las siguientes actividades:

1. Se importaron las bibliotecas necesarias (pandas, numpy, matplotlib, seaborn, scipy y sklearn).
2. Se cargo el archivo advertising.csv y se realizo una descripcion estadistica del conjunto de datos.
3. Se analizaron los posibles valores atipicos mediante boxplots.
4. Se realizaron graficos de dispersion entre las variables independientes (TV, Radio y Newspaper) y la variable dependiente (Sales) para observar su relacion lineal.
5. Se calculo la matriz de correlacion y se visualizo mediante un mapa de calor.
6. Se calculo el VIF (Factor de Inflacion de Varianza) para cada variable y se grafico para analizar posibles problemas de multicolinealidad.
7. Se construyo un modelo de regresion lineal multiple considerando las tres variables (TV, Radio y Newspaper).
8. Se interpretaron el intercepto y los coeficientes del modelo para comprender el efecto de cada variable.
9. Se analizaron los residuos mediante histogramas y graficos Q-Q para verificar la normalidad.
10. Se verifico la homocedasticidad graficando los residuos contra los valores predichos.
11. Se calcularon las metricas de desempeno MSE, RMSE y R2 para evaluar la precision del modelo.
12. Se graficaron las ventas reales contra las predichas para evaluar visualmente el nivel de ajuste.
13. Se ajusto el modelo con statsmodels para obtener los valores p y determinar la significancia estadistica de cada variable.
14. Se construyo un modelo sin la variable con mayor multicolinealidad (sin Radio) y se evaluo nuevamente el ajuste.
15. Se construyo un modelo sin la variable sin relacion lineal (sin Newspaper) y se evaluaron los resultados.
16. Finalmente, se compararon los tres modelos y se concluyo cual fue el mejor y cuales variables influyen mas en las ventas.

---

### Como se obtuvieron los resultados:
- Se importaron las librerias pandas, numpy, seaborn, matplotlib, scipy y sklearn.
- Se cargo el dataset advertising.csv desde Google Drive.
- Se aplicaron metodos de analisis exploratorio y visualizacion de datos (boxplots, mapas de calor, graficos de dispersion).
- Se construyeron modelos de regresion multiple y se interpretaron los coeficientes.
- Se verificaron los supuestos del modelo mediante el analisis de residuos, homocedasticidad y graficos Q-Q.
- Se calcularon las metricas de desempeno (MSE, RMSE y R2).
- Se compararon los modelos completos, sin multicolinealidad y sin variables no lineales.
- Se redactaron las conclusiones finales sobre el mejor modelo y las variables con mayor influencia.

---

### Para reproducir los resultados:
1. Abrir el archivo Practica22_SergioTrejo.ipynb en Google Colab o Jupyter Notebook.
2. Cargar el archivo advertising.csv en la ruta correspondiente.
3. Ejecutar todas las celdas en orden.
