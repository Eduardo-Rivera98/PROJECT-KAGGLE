# PROJECT-KAGGLE
Este proyecto consiste en coger una dataset de kaggle, y a través de feature engineering y limpieza, buscar un modelo de machine learning que dé el error cuadrado medio mínimo posible.
![alt text](https://d500.epimg.net/cincodias/imagenes/2021/06/25/companias/1624630363_897564_1624630510_noticia_normal.jpg "Logo Title Text 1")

### Primer paso: Limpieza y feature engineering
El primer paso era abrir el dataset y ver cuáles eran los datos. Nos encontramos con muchos categóricos, para los cuáles me tuve que meter en internet para saber el orden que tenían cada uno y poder asignarles un valor. Lo siguiente era mirar la correlación de cada una de las variables, para detectaar así colinealidad. Inicialmente boorraremoss las tres variables con una alta correlación, aunque luego veremos que esto empeora nuestro modelo.
### Segundo paso: Probar modelos
Lo siguiente que habrá qque hacer es probar distintos modelos a ver cuál nos da el error cuadrado medio más bajo. Comenzaremos por un modelo de regresión lineal, dado que es el primero y más simple que hemos visto. Vemos que da un error muy alto, asi que pasaremos a probar con Ridge(), Lasso(), SGDRegressor(), KNeighborsRegressor(), y GradientBoostingRegressor(). El último de estos dará un error notablemente inferior al resto, por lo que de momento será nuestro mejor modelo. Es en este punto dónde decido probar a quitar columnas o dejarlas y a estandarizar o normalizar los datos de la columna 'table' y 'depth'. Tras mucho ensayp y error, parece que lo óptimo es dejarlo como está.
Continuo mi investigación con modelos de random forest, para hacer arboles de decisión. Aquí vuelven a mejorar nootablemente los resultados, y probando distintas cosas con los parámetros acabo con un rmse de 562. Finalmente decido investigar con la librería h2o que me exige conectarme a java. Probando distintas extensiones de la librería, acabo descrubiendo que la más útli será auto ML, dado que va a probar con numerosos modelos a la vez y puedo seleccionar que me dé aquel con menor rmse. Aquí me tocó probar de nuevo con distintos trains, para ver cual me daaba un modelo más ajustado.
### Tercer paso: Exportar resultados y subirlos
Había que hacer un csv con las predicciones de precio y el id del diamante, y subrilo a kaggle, ahí te daría el rmse real.

