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
