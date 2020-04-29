# ICU Mortality Prediction 

Partiendo de los datos disponibles del Datathon 2020. Vamos a intentar crear un modelos que utilicen los datos de las primeras 24h en la UCI para predecir la probabilidad de supervivencia de los pacientes.

## Base de datos 
Se encuentra en kaggle dentro del challenge *WiDS Datathon 2020*:
[Link](https://www.kaggle.com/c/widsdatathon2020/data)	

## Descripción 
Hemos dividido el proyecto en 3 Notebooks de python diferentes:
* ICU Mortality Prediction Visualization Notebook, donde visualizamos todas las variables
* ICU Mortality Prediction Preprocessing Notebook, donde preprocesamos cada los datos 
* ICU Mortality Prediction Classification Notebook, donde implementamos diferentes clasificadores 
## Pipeline 
A continuación se puede ver el pipeline que hemos seguido en el proyecto:


**1. General info**

* df visualisation (ICU Mortality Prediction Visualization Notebook)

*  drop variables with a lot of missing values (ICU Mortality Prediction Preprocessing Notebook)
  
  
**2. Remove outliers** (ICU Mortality Prediction Preprocessing Notebook)


**3. Replace missing values** (ICU Mortality Prediction Preprocessing Notebook)


**4. One Hot Encoding** (ICU Mortality Prediction Preprocessing Notebook)


**5. Normalisation** (ICU Mortality Prediction Classification Notebook)

* x, y and train_test_split 

* Standarisation 

**6. Feature Selection** (ICU Mortality Prediction Classification Notebook)

* Feature importance

* Algoritmo univariante --> Prueba F de Fisher

* Eliminación Recursiva de atributos --> 
 
 **7. Unbalanced** (ICU Mortality Prediction Classification Notebook)
    
* Undersampling

* Oversampling
 
 **8. Classification** (ICU Mortality Prediction Classification Notebook)
 
* LDA (Fisher)
 
* Mayoría de votos
 
* Boosted trees
   
* Random forest
    
 **9.Comparison**(ICU Mortality Prediction Classification Notebook)
 
 ## ICU Mortality Prediction Visualization Notebook 
 En este cuaderno visualizamos las variables utilizando histogramas y diagramas de dispersion
 
 
 ![Image](http://url/a.png)

 ## ICU Mortality Prediction Preprocessing Notebook
 En este cuaderno hemos preprocesado cada variable de forma independiente identificando los outliers e imputando los valores nulos. También hemos eliminado las variables con valores unicos y aquellas que tenían más de un 60% de valores nulos
 
 
 Otra etapa del preprocesado ha sido el *One Hot Encoding* para las codificar las variables categoricas. 
 
 
 Una vez que tenemos los datos preprocesados los guardamos como una nueva base de datos: 
 `clean_data.to_csv('pre_ICU_Mortality_Prediction.csv')`
 
 ## ICU Mortality Prediction Classification Notebook
 En este cuaderno vamos a implementar los clasificadores para ello:

1. Dividir en train y test 


2. Balancear los datos por random *oversampling* y *undersampling*


3. Vamos a implementar 4 tipos de clasificadores: LDA, Mayoría de votos, Boosted Trees, Random Forest y SVM


4. Además vamos a disminuir el numero de características mediante: seleccion univariante de caracteristicas y un algoritmo recursivo, para ver si mejoran las prestaciones.

## Resultados 
Vamos a analizar las prestaciones de los clasificadores mediante las curvas ROC y las matrices de confusión.


## Presentación
Presentación de Overleaf para información más detallada


 
 
 
 
