# Capstone Project -1 - Appliances Energy Prediction
## Overview

Business Problem Description – Dataset contains the house temperature and humidity conditions were monitored with a ZigBee wireless sensor network. As per the description on UCI website, each wireless node transmitted the temperature and humidity conditions around 3.3 min, Then, the wireless data was averaged for 10 minutes periods. The energy data was logged every 10 minutes with m-bus energy meters. Combining this data with the weather data based on the date time columns

To find the key feature from the dataset which contributes to the most and the 

1.	Predict the appliance energy consumption.
		a.	With collected data of temperature and humidity (indoor and outdoor) sensors.
		b.	Weather data collected
		c.	Fuel price over the period of time.
2.	Best prediction model with best parameter for future prediction of the appliance Energy.

**Dataset Details –**

There are 19735 and 29 attributes.  Weather from the nearest airport weather station (Chievres Airport, Belgium) was downloaded from a public data set from Reliable Prognosis (rp5.ru). There are 2 random variables, which has be explored more.

Another dataset used is to about the fuel price on the year of 2016, integrating this with overall dataset will help understand the fuel price impact the appliance energy consumption.

## Implementation Approach –

 - Load the dataset and perform the EDA, and merge with the dataset of Oil price for the particular date range. 
	 - 	Various Data cleaning and feature engineering has been performed based on previous enhancements.
	 - Missing value has been updated with 

* Experiments and Implement the best performing model
	* We will initially create the a benchmark model, using the linear regression algorithm
	* We will calculate the RMSE and R^2 score.
	* Lets update the data and scale the data.
	* Now lets create the following models with key important features –
	* Regularized linear models as an improvement over Linear Regression.
		* Ridge Regression
		* Lasso Regression
	* Ensemble based Tree Regression models, which deal with number of features and outlier data.
		* Random Forests
		* Gradient Boosting
		* Extra Trees
		* Neural networks for non-linear relationships target feature and predictors.
		* Multi-Layer Perceptron

* Comparing the Score and visualization on the performance of different algorithm, we will select the best performing algorithm

* Hyper-parameter tuning the best Model observed from step4 –
	* Model tuning – Using the RandomizedSearchCV, tune to model and evaluate the model accuracy by calculating the root mean square error.

* We will find out the important features contributing from the data set
	* Will generate the visualization of the features with high to low importance of the features.

* Feature and Model Evaluation- we will try to clone the above best model clone and do a prediction only with the most important feature, to verify if there is any improvement in the model accuracy.
