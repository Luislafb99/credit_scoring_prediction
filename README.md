# 📌Credit Scoring Prediction💳📊

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


## 📌Configuración del entorno

En este proyecto, emplearemos el lenguaje de programación Python junto con sus bibliotecas fundamentales, como pandas, seaborn, matplotlib y sklearn.

Definiremos dos variables globales clave:

-**df_banco**: Almacenerá una copia de la base de datos que contiene el historial crediticio de los clientes, una medida preventiva para gestionar eficientemente los datos.

-**resultados**: Un diccionario que se utilizará para almacenar las métricas de rendimiento de los modelos, facilitando la comparación entre ellos.


## 📌Preprocesamiento de datos

En este apartado, nos enfocaremos en la detección y eliminación de posibles entradas duplicadas, así como en el manejo de datos nulos utilizando la biblioteca pandas. Además, ejecutaremos la conversión de valores categóricos a numéricos. Todas estas operaciones serán llevadas a cabo de manera eficiente dentro de la función **procesar_datos()**.


## 📌Exploración de datos 📊

En el proceso de Análisis Exploratorio de Datos (EDA), nos propusimos evaluar si variables como sexo, edad, tiempo de pago del crédito y monto son significativas. Para realizar esto, filtramos los datos y creamos nuevos atributos dentro de la función feature_engineering().

A continuación, presentamos algunos datos relevantes visualizados:
<p align="center">
<img width="755" alt="image" src="https://github.com/Luislafb99/credit_scoring_prediction/assets/152426197/8122e58f-1070-4461-bf8f-28095f0cec03">
</p>
La variable objetivo es Default, donde 0 indica que un titular no es moroso y 1 indica que sí lo es. Observamos un desbalance en los datos, ya que contamos con 700 buenos clientes y 300 malos clientes. Para abordar este desequilibrio, optamos por utilizar SMOTE, una técnica diseñada para contrarrestar el desbalance de clases en conjuntos de datos. Esto ayudará a reducir el sesgo asociado a la clase subrepresentada, mejorando así los resultados de nuestros modelos. Para implementar SMOTE, utilizaremos la librería imblearn.over_sampling.

Además, examinamos la correlación entre las variables, especialmente con respecto a Default:

<p align="center">
<img width="741" alt="image" src="https://github.com/Luislafb99/credit_scoring_prediction/assets/152426197/026ca2f8-9382-452d-8c30-930abad54b74">
</p>

Observamos que algunos atributos pueden ser eliminados después de la creación de los nuevos atributos mencionados anteriormente, por lo tanto, procedimos a eliminarlos.

Este análisis nos permitirá tomar decisiones informadas sobre qué variables son más relevantes para nuestros modelos y realizar las modificaciones necesarias para mejorar la calidad de los datos.

## 📌Construcción de modelos

En la construcción de modelos, dividimos entre datos de entrenamiento(train) y datos de prueba(test) y normalizamos los datos, esto para poder tener mejores resultados con la implementación de los modelos.
Las librerias y métodos que se usaron fueron:
<p align="center">
<img width="466" alt="image" src="https://github.com/Luislafb99/credit_scoring_prediction/assets/152426197/fecd73c9-a727-4ae1-90cc-cbc2eb1fa925">
</p>
De estos métodos usamos .fit() y .prediction(), para entrenar y realizar predicciones con los datos que tomamos como x_test.

Los resultados se muetran en las siguientes matrices de confusión:
<p align="center">
<img width="762" alt="image" src="https://github.com/Luislafb99/credit_scoring_prediction/assets/152426197/f18cc726-b96a-4222-8fb1-b2cf5b46c07d">
</p>

## 📌Evaluación y selección de modelos

Para la selección de modelos tomamos las metricas de Accuracy, Recall, Precisión, F1_Score y Auc_Roc.
<p align="center">
<img width="740" alt="image" src="https://github.com/Luislafb99/credit_scoring_prediction/assets/152426197/0c179942-993d-4558-8428-7b08b0770370">
</p>

El modelo KNN destaca en términos de precisión general (accuracy), precisión en la identificación de clientes morosos (precision), y equilibrio entre precisión y capacidad para identificar morosos (F1_Score). Aunque el modelo de árbol de decisión tiene un recall ligeramente superior (capacidad para identificar morosos), el KNN logra un buen equilibrio entre todas las métricas. Por lo tanto, basándonos en el conjunto de métricas y considerando los objetivos del negocio, el modelo KNN parece ser la elección preferida.




Este proyecto utiliza el conjunto de datos "German Credit data". La información sobre la fuente original de los datos es la siguiente:

- **Título:** German Credit data
- **Fuente:** Professor Dr. Hans Hofmann, Institut f"ur Statistik und "Okonometrie, Universit"at Hamburg, FB Wirtschaftswissenschaften, Von-Melle-Park 5, 2000 Hamburg 13








