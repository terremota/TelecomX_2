
# Análisis de Evasión de Clientes - Telecom X (Parte 2)

Esta Parte 2 se centra en la preparación avanzada de datos, el análisis de correlación y la construcción de modelos predictivos para identificar a los clientes que podrían de cancelar su servicio
Proyecto de Análisis de Evasión de Clientes - Telecom X (Parte 2)

1. Introducción
   
Este proyecto forma parte del desafío Telecom X y se enfoca en el análisis y la predicción de la evasión (churn) de clientes. La Parte 2 se centra en la preparación avanzada de datos, el análisis de correlación y la construcción de modelos predictivos para identificar a los clientes en riesgo de cancelar su servicio.

2. Datos
   
Se utiliza el archivo TelecomX_normalizado.csv, resultado de la limpieza y organización de datos realizada en la Parte 1 del desafío. Este conjunto de datos contiene información sobre clientes de una empresa de telecomunicaciones, incluyendo datos demográficos, servicios contratados, información de cuenta y el estado de evasión (Churn).

3. Preparación de Datos
   
Se realizaron las siguientes etapas de preparación de datos:

* Extracción de Datos: Carga del archivo TelecomX_normalizado.csv.
* Eliminación de Columnas Irrelevantes: Se eliminó la columna customerID.
* Encoding: Transformación de variables categóricas a formato numérico utilizando One-Hot Encoding para la mayoría y Label Encoding para la variable objetivo Churn. Se manejaron los valores nulos en Churn y se convirtió account.Charges.Total a numérico, rellenando nulos si aparecían después de la conversión.
* Verificación de la Proporción de Cancelación (Churn): Se analizó el desbalance de clases en la variable objetivo.
* Normalización/Estandarización: Se aplicó StandardScaler a las variables numéricas (customer.tenure, account.Charges.Monthly, account.Charges.Total) para preparar los datos para modelos sensibles a la escala.

4. Correlación y Selección de Variables
   
* Se realizó un análisis de correlación para entender las relaciones entre las variables numéricas y la variable objetivo Churn.

* Se visualizaron las correlaciones con un mapa de calor.
* Se interpretaron las correlaciones, destacando la relación negativa entre customer.tenure y Churn, y la relación positiva entre account.Charges.Monthly y Churn.
* Se analizó la correlación entre las variables predictoras, observando una alta correlación entre customer.tenure y account.Charges.Total.
* Se investigaron relaciones específicas con Churn mediante boxplots y scatter plots.

5. Modelo Predictivo
Se dividió el conjunto de datos en entrenamiento y prueba (80/20) y se entrenaron y evaluaron varios modelos predictivos:

*Regresión Logística: Modelo basado en la escala de los datos, entrenado con datos estandarizados.
*Random Forest: Modelo basado en árboles, entrenado sin estandarización.
*KNN: Modelo basado en distancia, entrenado con datos estandarizados y PCA.
*Árbol de Decisión: Modelo basado en árboles, entrenado sin estandarización.

La evaluación se basó en métricas como Exactitud, Precisión, Recall, F1-score y Matriz de Confusión, prestando especial atención al rendimiento en la clase minoritaria (Churn = 1) debido al desbalance.

6. Resultados y Evaluación de Modelos
* Se presentaron los resultados de cada modelo, comparando su desempeño.

Se identificó la Regresión Logística como el modelo con mejor desempeño para detectar cancelaciones (Recall y F1-score más altos para Churn=1), a pesar de tener una exactitud general ligeramente menor que Random Forest.

7. Interpretación y Conclusiones
* Se analizaron las variables más importantes para la predicción de churn, destacando su influencia en los modelos.

* Se resumieron los principales hallazgos del análisis y de la evaluación de modelos.

8. Estrategias de Retención
Basándose en los factores clave identificados en el análisis y la importancia de las variables, se propusieron estrategias concretas para reducir la cancelación de clientes:

* Fomentar contratos a largo plazo.
* Reducir la insatisfacción por costos altos.
* Enfocarse en clientes nuevos.
* Mejorar la experiencia con fibra óptica.
* Optimizar métodos de pago.

#. Tecnologías Utilizadas
* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* 
10. Autor
Pablo Ortega / terremota
