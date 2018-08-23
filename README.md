## Project Description
This project is about managing savings for a truck company with a larger fleet of trucks. As a data scientist, I needed to understand and  analyze the historic data, define a potential business case, develop and analyze a predictive model and present the results. 
### Understanding and analyzing the data
We accessed the database that was restored from the [Historical Gas Station Information](https://creativecommons.tankerkoenig.de/) from 2.5.2016 till 27.7.2018 using pgAdmin. We noticed that there are 3 types of gasoline: diesel, e5 and e10. Some questions were answered to get to know the data better, such as how many different brands are there on the gas stations and what are the minimum, maximum and average price of each gasoline per month as well as their distribution.  
### Defining a possible business potential
In this part of the project, we proposed some business ideas with a goal of benefiting the company. Some of the ideas proposed were:
 - Increase trucks' travalled distances during periods of the year in which gasoline prices are cheaper and vice versa.
 - Select gas stations on the same road/path that offer cheaper gasoline prices.
 - Select roads/paths where there are gas stations that offer cheaper gasoline prices.
 - Prevent trucks from driving during rush hours.
 - Use trucks that consume the cheapest gasoline type more often than other trucks.
We proceeded with idea No.1 which is to increase trucks' travalled distances during periods of the year in which gasoline prices are cheaper and vice versa.
According to data that are given, we were able to tell the average price per liter for the year 2017 for Diesel, E5 and E10 and together with data about the average truck consumption and truck fleet milage we made calculations in order to tell if our idea will give some cost benefits to the company.
Instead having the same average milage per month we adapted it according to the average fuel price per month and the results showed that it saved approximately 6 million € per year for the entire fleet.
### Developing a predictive model
We proceeded then to train a model to predict the price of Diesel only, without loss of generality. We used the average price per day as input to the model  because we thought that hourly price was not of a big meaning.
Before training model we pre-processed the data. We did the following operations:
 - Fill in the missing values
 - Stationarity check
 - Feature extraction
 - Split the data into a training set (70%) and a test set (30%)
 - Normalize the training data
### Analyzing the results
For our trained models we used Linear Regression, Ridge Regression, Lasso Regression and XGB Regression models and we saved 30% of the data for testing. Important measurements for quality of predictions are: MAPE(mean absolute percentage error), R squared (coefficient of determination (in econometrics it can be interpreted as a percentage of variance explained by the model)) and MSE(mean squared error). According to our results, XGB Regression gave us the worst results because MAPE is higher and R squared lower than with other models. Lasso Regression is second worst because of a bit lower R squared and a bit higher MAPE, while Linear Regression and Ridge Regression obtain the same results.

## Prerequisites for the project
```
Python 3.6.4
Numpy
Pandas
Sklearn
Statsmodels
XGBoost
Seaborn
Matplotlib
```
