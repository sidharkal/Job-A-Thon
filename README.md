
# Jobathon April 2022
## Problem Statement

ABC is a car rental company based out of Bangalore. It rents cars for both in and out stations at affordable prices. The users can rent different types of cars like Sedans, Hatchbacks, SUVs and MUVs, Minivans and so on.

In recent times, the demand for cars is on the rise. As a result, the company would like to tackle the problem of supply and demand. The ultimate goal of the company is to strike the balance between the supply and demand inorder to meet the user expectations. The company has collected the details of each rental. Based on the past data, the company would like to forecast the demand of car rentals on an hourly basis.

## Objective

The main objective of the problem is to develop the machine learning approach to forecast the demand of car rentals on an hourly basis.

## Approach

The data given had no features except date and hour. It was a pure time series problem. There were missing values inbetween as well i.e., dates and hours where the demand was not given. There were a couple of approaches that could be tried:
* Use ARIMA to forecast.
* Perform feature engineering and build an ML model to predict.

### Time series approach

The main problem in this apporach was the stationarity of the time series. I tried to make the series stationary by applying transformations such as log returns, boxcox. But the results were not satisfactory. One more issue with using ARIMA to forecast was that we were supposed to forecast for around 13 months on an hourly basis. ARIMA failed to do it for such a long time period.

### ML Approach

Before building an ML model, feature engineering was done. Basic time related features such as day, month, hour, weekofyear, dayofyear, weekday were created. Aggregated lag features were also created but it did not help imporve score much as there were many missing values.

here i used Arima,LSTM and automl model with (pycaret) model 
