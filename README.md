🚀 Predicción de Baja de Clientes (Churn) - Desafío Telecom X2
🎯 Objetivo del Proyecto

Este proyecto de Data Science tiene como finalidad desarrollar un modelo de Machine Learning capaz de predecir el Churn (abandono o cancelación de servicio) de los clientes de una empresa de telecomunicaciones. El objetivo principal es identificar a los clientes con mayor riesgo de cancelación para que la empresa pueda implementar estrategias de retención proactivas.
💾 Fuente de Datos

Los datos utilizados provienen de un conjunto de datos tratado previamente en la primera parte del desafío Challenge Telecom X.

    Dataset: Datos de clientes de telecomunicaciones.

    Target (Variable a Predecir): Churn (Sí/No, convertido a 1/0).

🛠️ Metodología

El análisis y modelado se llevaron a cabo siguiendo un flujo estándar de Data Science:

    Extracción y Limpieza: Carga de datos, conversión de variables categóricas a numéricas (Yes/No a 1/0), y manejo de valores faltantes (imputación con 0).

    Preparación de Datos (Feature Engineering): Se realizó la codificación de variables categóricas nominales utilizando One-Hot Encoding (pd.get_dummies).

    Normalización de Características: Se aplicó el método MinMaxScaler a las variables numéricas para escalar los datos, un paso crucial para modelos basados en distancias como KNN y Regresión Logística.

    Modelado Predictivo: Se evaluaron y compararon cuatro modelos de clasificación diferentes.

📊 Modelos Evaluados y Resultados

Se entrenaron y evaluaron los siguientes modelos para determinar el más adecuado para predecir el Churn:
Modelo	Accuracy (Precisión)	F1-Score	Precisión	Recall (Sensibilidad)
Dummy Classifier (Baseline)	0.7489	0.0000	0.0000	0.0000
Decision Tree	0.7489	0.6019	0.5520	0.6598
K-Nearest Neighbors (KNN)	0.7672	0.6122	0.6091	0.6152
Regresión Logística	0.7937	0.6358	0.6558	0.6171
🏆 Conclusión del Modelo

El modelo de Regresión Logística demostró el mejor desempeño general, con la Accuracy más alta (0.7937) y un buen equilibrio en el F1-Score y Precisión.
💡 Insights y Conclusiones Clave

El análisis de correlación y la interpretación del modelo revelaron que las siguientes variables son las más influyentes en la decisión de un cliente de cancelar el servicio:

    Antigüedad del Cliente (customer.tenure): Los clientes con menor antigüedad tienden a cancelar más.

    Cargos Mensuales (account.Charges.Monthly): Clientes con facturaciones mensuales más altas muestran una mayor propensión al Churn.

    Servicio de Fibra Óptica (internet.Fiber optic): La fibra óptica apareció como un factor sorpresa; mientras mayor es su uso, mayor es la propensión a la cancelación, lo cual puede estar relacionado con el alto costo de este servicio.

    Uso de Soporte Técnico (internet.TechSupport): Los clientes que cancelan tienen un menor uso de soporte técnico, lo que sugiere una oportunidad para la empresa de mejorar este servicio como herramienta de retención.

💻 Tecnologías Utilizadas

    Python

    Pandas

    NumPy

    Scikit-learn (Para modelos, train_test_split, métricas y normalización)

    Seaborn y Matplotlib (Para visualización y matriz de correlación)
