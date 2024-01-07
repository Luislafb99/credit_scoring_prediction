# Credit Scoring Prediction

Uno de los mayores desafíos en las entidades financieras es lidiar con clientes morosos. La solución más eficaz es abordar este problema antes de otorgar un crédito.

<p align="center">
  <img src="https://github.com/Luislafb99/credit_scoring_prediction/assets/152426197/c7981011-de08-4aa4-8c7b-499df41e90c5" alt="Prediction Image" style="display:block; margin:auto; width:30%;" />
</p>

**¿Cómo prevenimos este problema?**

La prevención se logrará mediante predicciones sobre nuestros clientes. Utilizando los datos disponibles de los clientes, anticiparemos si serán buenos clientes o si presentarán problemas de morosidad. Este proceso se llevará a cabo mediante modelos de machine learning.

Dentro de nuestra base de datos, compararemos el rendimiento de tres modelos de machine learning para determinar cuál es más efectivo en este escenario. Los modelos que evaluaremos son:
- K - Nearest Neighbors
- Naive-Bayes Bernoulli
- Árboles de Decisión

Este análisis nos permitirá seleccionar el modelo más adecuado para predecir y gestionar el riesgo crediticio de manera eficiente.


## Configuración del entorno

En este proyecto, emplearemos el lenguaje de programación Python junto con sus bibliotecas fundamentales, como pandas, seaborn, matplotlib y sklearn.

Definiremos dos variables globales clave:

-**df_banco**: Almacenerá una copia de la base de datos que contiene el historial crediticio de los clientes, una medida preventiva para gestionar eficientemente los datos.

-**resultados**: Un diccionario que se utilizará para almacenar las métricas de rendimiento de los modelos, facilitando la comparación entre ellos.


## Preprocesamiento de datos

En esta sección, abordaremos la eliminación de posibles entradas duplicadas y la gestión de datos nulos mediante el uso de la biblioteca pandas. Además, llevaremos a cabo la conversión de valores categóricos a numéricos. Todo este proceso se realizará dentro de la función **procesar_datos()**.


## Exploración de datos

Se tomara 




















Este proyecto utiliza el conjunto de datos "German Credit data". La información sobre la fuente original de los datos es la siguiente:

- **Título:** German Credit data
- **Fuente:** Professor Dr. Hans Hofmann, Institut f"ur Statistik und "Okonometrie, Universit"at Hamburg, FB Wirtschaftswissenschaften, Von-Melle-Park 5, 2000 Hamburg 13








