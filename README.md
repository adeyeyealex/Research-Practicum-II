# Research-Practicum-II
TIME SERIES FORECASTING OF FINANCIAL MARKET 

Table of content:
1.	Introduction
2.	Import libraries and load. 
3.	Data Visualization 
4.	Feature Engineering 
5.	Data Preparation 
6.	Model Creation 
7.	Model Evaluation 
8.	Conclusion

Introduction
The project will look at the different stock prices based upon the trend in the market for the 10 years to determine or make an accurate prediction of what the prices of stocks will look like in the foreseeable future. What we mean here is that the historical data will be used as a training set, the behavior will be learned over several iterations which will in turn be used to predict the future outcome. Dataset will be collected from yahoo finance website for the US stock exchange for both Microsoft and Gold price. Additional factors such as inflation and unemployment rate will also be considered during the project to know how this affects the price of the stock.

Import libraries and load
Some of the relevant libraries used are:
•	Pandas
•	Numpy
•	Datetime
•	MinMaxScaler
•	Sklearn
•	Tensorflow
•	Matplotlib
•	Seaborn

Data Visualization 
We could see that there are high correlations between Microsoft stock price and the price of the economic indicators Inflation rate. Unemployment has a very low correlation to the Microsoft stock price. 
Some of the features were therefore dropped since there seemed to be low or no relationship with target variable which is going to be the Adj Close of the Microsoft stock. The features that will be used will just be Inflation rate and gold price. 

Feature Engineering 
Some modifications were done adding some features such the days of the week, the months of the year and the years on the years’ time frame for the project. This was done for seasonal check of when people tend to buy commodities. it deduced from the plots made that people buy more stocks towards the first quarter of the year.

Data Preparation
Relevant columns were selected for analysis which are MSFT stock price, Inflation rate and Gold price. The data was split into training, validation and test sets. Helper function was created for the model creating a list of X and Y array. Time_steps of 1 was also used, using 1 as the sequence of time_steps of consecutive observation. 70% of the data was used for training, 20% for test and 10% for validation set.

Model Creation
LSTM model was used with sequential model architecture. Adem and RMSprop optimizers were used and measn squared error was used as the loss function. The model was fitted on the training data. Evaluation of the model was done on the validation and the test data. Predictions were then made and plot comparing the actual data and the trained data.
Also, Xgboost, Random Forest and SVR were also used to train the training data. And testing were also done on the test data. PLots weere also made.

Model Evaluation
The performance of the LSTM models were evaluated using various metrics such as mean squared error, mean absolute error, and root mean squared error. The loss were also checked on each of the data(training, validation and test sets). Visualize the actual and predicted values of the MSFT stock price using a line plot.

Conclusion
From the LSTM model, we see that adding more layers and a low learning rate will improve the efficiency of the model. Among the optimizers used, Adam seems to be more efficient than the other optimizers. We could also say increasing the epochs does not improve the model. We also see that the tree models such as Xgboost, Random etc. will have difficulty solving time series model as we could see that the predictions flat out. Differencing the target might make a difference in the result if it was done. Some feature that could also be added to aid prediction could be sentiment analysis example include Game stop stock price years back.

In this project, we were able to analyze and predict the MSFT stock price using various economic indicators such as inflation rate and gold price. We created an LSTM model that was able to capture the complex patterns and trends in the data. Time series can be used for various fields such as finance, economics and business to make informed decisions and predict future trends.



