# Aplicación de técnicas de machine learning para el mantenimiento predictivo

Proyecto final de carrera

## 1. Resumen del trabajo
Uno de los grandes problemas en los procesos de fabricación es la rotura de suministro, uno de estas causas es el fallo de las maquinarias de fabricación. Actualmente la solución más común es la realización de mantenimientos periódicos, cuyo método conlleva a un coste constante donde la mayoría de los casos es innecesario.
En este proyecto se estudia cómo puede las técnicas de análisis de datos avanzadas pueden contribuir en la prevención de estas roturas mientras se reducen el coste de mantenimientos constantes e innecesarios. En concreto se aplicarán estas técnicas para encontrar una solución analítica, con el fin de predecir cuándo una máquina fallara y así poder actuar antes de que ocurra dicho fallo, para prevenir cortes en el proceso de fabricación.

## 2. Análisis inicial y procesamiento previo
Para exploración de de Datos, se ha realizado un estudio con la explocaració de los datos. Disponible en el archivo:

TFM2.ipynb
TFM2.html

Resumen de la EDA realizada:

- Introducción de los datos de origen
- Muestra los 5 archivos CSV originales.
- Dimensiones de los datasets
- Verificación de valores nulos
- Verificación de valores duplicados
- Verificación de falta de datos
- Exploración Telemetry
    - Variación de las medidas a lo largo del tiempo
    - Distribuciones de las medidas
- Exploración de Machine
    - Cantidad y modelos disponibles
    - Visualización de los modelos por edad
- Exploración de Errors
    - Cantidad y errores registrados
    - Visualización de los errores por maquina y tiempo
- Exploración de Failure
    - Cantidad y fallos registrados
    - Visualización fallos por dia, mes y año
- Exploración de Maintenance
    - Cantidad y mantenimientos registrados
    - Visualización mantenimientos por dia, mes y año

A su vez se ha realizado una función que combina los 5 archivos CSV en uno solo mediante uniones de los juegos de datos y una tabla resumen.

Una vez explorados los datos, se ha realizado una función para filtrar y generar únicamente series temporales sin fallos, dependiendo de su modelo, edad y máquina. También se ha creado las variables de objetivo como el RUL de la máquina y el estado de trabajo de la máquina.
Disponible en el archivo:

TFM_GenerateDatasets_v2.ipynb
TFM_GenerateDatasets_v2.html


## 3. Análisis y modelado
Se ha seleccionado un conjunto de modelos de las cuales se ha seleccionado los siguientes:

En el archivo encontramos los regressores:
TFM_Regressors_Ordered.ipynb
TFM_Regressors_Ordered.html
TFM_Regressors_RandomizedLogs.ipynb
TFM_Regressors_RandomizedLogs.html
TFM_LSTM_Models_Regressor_Cut.ipynb
TFM_LSTM_Models_Regressor_UnCut.ipynb

Regression:
- Linear regression
- Support-vector machines
- Random forest
- Gradient boosting
- Extreme gradiend boosting
- Long-Short Term Memory

En el archivo encontramos los clasificadores:
TFM_Classifiers.ipynb
TFM_Classifiers.html
TFM_LSTM_Models_Classifier_Cut.ipynb
TFM_LSTM_Models_Classifier_UnCut.ipynb

Clasificación:
- Logistic regression
- Support-vector machines
- Random forest
- Gradient boosting
- Extreme gradiend boosting
- Long-Short Term Memory

## 4. Resultados
En los mismos archivos de los modelos encontramos los resultados obtenidos de los modelos. Para evaluar los modelos se ha utilizado:

Regression:
- Coeficiente de determinación
- RMSE
- MSE
- MAE

Clasificación:
- Precision
- Recall
- F1 score
- Accuracy
- Curva ROC AUC
