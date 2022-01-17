# PROJECT-KAGGLE
This project was a competition between the 26 members of my class. With a dataset from Kaggle about diamonds, we had to develop a machine learning model to predict the prices of the diamonds. The objective was to use feature engineering to develop a model with the lowest root mean squared error (rmse) possible. For my class I was the one to obtain the lowest rmse, winning the first prize.
![alt text](https://d500.epimg.net/cincodias/imagenes/2021/06/25/companias/1624630363_897564_1624630510_noticia_normal.jpg "Logo Title Text 1")

### First step: Data cleaning and feature engineering
The first step was to open the dataset and explore the data. There were many categorical features, which gave information about the quality of the diamonds. To interpret these features and classify them with the according values, I had to go to the internet. Next I had to study the possible autocorrelation between variables, detecting possible colineality.

### Second step: Trying different models
I started trying different models to see with which one I obtained the lowest rmse. My first model was a linear regression one, as it is the simplest of the ones I have studied, however the high rmse obtained told me this was not the way to proceed. The next ones I tried were Ridge(), Lasso(), SGDRegressor(), KNeighborsRegressor(), and GradientBoostingRegressor(). The last one of these gave back a significantly lower rmse, so here is where I started trying to take out different columns or standarizing data to see the effects on the model's precison. I then proceeded with Random Forest  and XGBoost models and trying different feature engineering methonds and messing with Hyperparametres, I finally ended up with a rmse of 562.
Finally, I decided to try H2o, and the AutoML library. This would give automatically the model with the lowest rmse.


