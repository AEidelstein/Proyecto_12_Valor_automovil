# Proyecto_12_Valor_automovil / Car_value
Valor de mercado del automóvil / Market value of a car

# Descripción del proyecto / Project description

SPA:

Rusty Bargain es un servicio de venta de coches de segunda mano que está desarrollando una app para atraer a nuevos clientes. Gracias a esa app, puedes averiguar rápidamente el valor de mercado de tu coche. Tienes acceso al historial, especificaciones técnicas, versiones de equipamiento y precios. Tienes que crear un modelo que determine el valor de mercado.

A Rusty Bargain le interesa:

   - la calidad de la predicción
   - la velocidad de la predicción
   - el tiempo requerido para el entrenamiento

EN:

Rusty Bargain is a used car sales service that is developing an app to attract new customers. Thanks to the app, you can quickly find out the market value of your car. You have access to history, technical specifications, equipment versions and prices. You have to create a model that determines the market value.

Rusty Bargain is interested in:

   - the prediction quality
   - the prediction speed
   - the requiered time for the training

# Instrucciones del proyecto / Project instructions

SPA:

   1. Descarga y examina los datos.
   2. Entrena diferentes modelos con varios hiperparámetros (debes hacer al menos dos modelos diferentes, pero más es mejor. Recuerda, varias implementaciones de potenciación del gradiente no cuentan como modelos diferentes). El punto principal de este paso es comparar métodos de potenciación del gradiente con bosque aleatorio, árbol de decisión y regresión lineal.
   3. Analiza la velocidad y la calidad de los modelos.

Observaciones:

   - Utiliza la métrica RECM para evaluar los modelos.
   - La regresión lineal no es muy buena para el ajuste de hiperparámetros, pero es perfecta para hacer una prueba de cordura de otros métodos. Si la potenciación del gradiente funciona peor que la regresión lineal, definitivamente algo salió mal.
   - Aprende por tu propia cuenta sobre la librería LightGBM y sus herramientas para crear modelos de potenciación del gradiente (gradient boosting).
   - Idealmente, tu proyecto debe tener regresión lineal para una prueba de cordura, un algoritmo basado en árbol con ajuste de hiperparámetros (preferiblemente, bosque aleatorio), LightGBM con ajuste de hiperparámetros (prueba un par de conjuntos), y CatBoost y XGBoost con ajuste de hiperparámetros (opcional).
   - Toma nota de la codificación de características categóricas para algoritmos simples. LightGBM y CatBoost tienen su implementación, pero XGBoost requiere OHE.
   - Puedes usar un comando especial para encontrar el tiempo de ejecución del código de celda en Jupyter Notebook. Encuentra ese comando.
   - Dado que el entrenamiento de un modelo de potenciación del gradiente puede llevar mucho tiempo, cambia solo algunos parámetros del modelo.

   - Si Jupyter Notebook deja de funcionar, elimina las variables excesivas por medio del operador del:

      del features_train

EN:

   1. Download and examine the data
   2. Train different models with various hyperparameters (you should make at least two different models, but more is better. Remember, several implementations of gradient boosting do not count as different models). The main point of this step is to compare gradient boosting methods with random forest, decision tree and linear regression.
   3. Analyse the speed and quality of the models.

Remarks:

   - Use the RECM metric to evaluate the models.
   - Linear regression is not very good for hyperparameter fitting, but it is perfect for a sanity check of other methods. If gradient boosting performs worse than linear regression, something has definitely gone wrong.
   - Learn on your own about the LightGBM library and its tools for creating gradient boosting models.
   - Ideally, your project should have linear regression for a sanity check, a tree-based algorithm with hyperparameter tuning (preferably, random forest), LightGBM with hyperparameter tuning (test a couple of sets), and CatBoost and XGBoost with hyperparameter tuning (optional).
   - Take note of the categorical feature encoding for simple algorithms. LightGBM and CatBoost have their implementation, but XGBoost requires OHE.
   - You can use a special command to find the execution time of the cell code in Jupyter Notebook. Find that command.
   - Since training a gradient boosting model can be time-consuming, change only a few parameters of the model.

   - If Jupyter Notebook stops working, eliminate the excessive variables by means of the operator of the:
      
      del features_train  
      

# Descripción de los datos / Data description

SPA:

El dataset está almacenado en el archivo /datasets/car_data.csv. -> archivo muy pesado para subirlo a GitHub.

EN:

The data set is stored in the file /datasets/car_data.csv. -> data is too heavy to be uploaded to GitHub.

## Características / Features

   - 'DateCrawled' — fecha en la que se descargó el perfil de la base de datos / date on which the profile was downloaded from the database
   - 'VehicleType' — tipo de carrocería del vehículo / vehicle body type
   - 'RegistrationYear' — año de matriculación del vehículo / vehicle registration year
   - 'Gearbox' — tipo de caja de cambios / Gearbox type
   - 'Power' — potencia (CV) / power (HP)
   - 'Model' — modelo del vehículo / vehicle model
   - 'Mileage' — kilometraje (medido en km de acuerdo con las especificidades regionales del conjunto de datos) / mileage (measured in km according to the regional specificities of the dataset)
   - 'RegistrationMonth' — mes de matriculación del vehículo / vehicle registration month
   - 'FuelType' — tipo de combustible / type of fuel 
   - 'Brand' — marca del vehículo / vehicle brand
   - 'NotRepaired' — vehículo con o sin reparación / vehicle with or without repair
   - 'DateCreated' — fecha de creación del perfil / date profile created
   - 'NumberOfPictures' — número de fotos del vehículo / number of pictures of the vehicle
   - 'PostalCode' — código postal del propietario del perfil (usuario) / profil owner (user) postal code
   - 'LastSeen' — fecha de la última vez que el usuario estuvo activo / last user activity date

## Objetivo / Objective

Price — precio (en euros) / price (in euros)
