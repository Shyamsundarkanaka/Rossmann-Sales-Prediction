# Rossmann-Sales-Prediction
In this project we have been given with the past data of major store chain Rossmann Drug stores and we have to build a model to predict the future sales. 

Sales Prediction is key aspect for all retail stores to maintain the right amount of production and inventory so that there is no shortage of goods and inventory costs are also optimized. 

There were 2 datasets one with the sales data and other with metadata of the 1115 unique stores. Shape of datasets: 
1.	Sales Data : 1017209 rows x 9 columns
2.	Store Data : 1115 rows x 10 columns

Data Cleaning: There are no null values in the sales data however there are few columns with null values in store data. Techniques like dropping the columns, filling the null values with mean values was used. A unique approach of filling the null values with latest date for date column was used, this helped in merging the datasets without altering the meaning provided by the data. 

Merging Datasets: As there are 2 data sets, it was merged on the common column Store Id. Left join was used to merge the dataset. The Shape of our final data is 1017209 rows x 14 columns

Exploratory Data Analysis was performed to obtain the insights of our dependent variable Sales. Various graphs were constructed comparing the Sales column with other columns. List of insights were obtained. 

Time Series Analysis was performed using seasonal_decompose from statsmodels.tsa.seasonal module. The graph of trend, seasonality and residual was plotted.

Feature Engineering - 1. One encoding and Label encoding was applied wherever necessary. 2.MinMaxScaler was used to scale the independent features. 3. Lastly month, year and day columns were extracted from the DateTime column. 

Modelling – Totally 6 models were build, hyperparameter tuning was performed on 2 models and cross validation was performed on 3 models. The list of models are:

1.	Linear Regression
2.	Lasso Regression
3.	Ridge Regression
4.	XGBoost Regression
5.	Stochastic Gradient Descent Regression
6.	Random Forest Regression


Conclusion: Random Forest Regressor model performs the best with an R2 Score of 0.968 with the best parameter of n_estimators 25. However, we can us estimator of 10 has it almost the same accuracy but reduces the computational time. Next the XGBoost gives the best with the R2 Score of 0.88.
