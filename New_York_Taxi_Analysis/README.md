# New York Taxi Analysis
Introduction of the project


## Problem Definition
Predict the aveage money spent on taxi rides for each region of New York per given day and hour
This problem is a a supervised regression problem. Supervised because we have the actual value of the value we' are trying to predict and regression because we're trying to predict us a continual variable (as opposed to categorical)

## Data 
Link to main dataset: 
[About TLC - TLC](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page)

Link to Weather data:
[Weather data](https://www.kaggle.com/datasets/aadimator/nyc-weather-2016-to-2022?resource=download)


## Data Cleaning 
Data points with negative and zero total_amount values were removed as they are not many of them, and they are likely faulty

Data points with very high total_amount values >= 200 were also removed 

## Data preparation

Extracted the transaction year, month, date, hour from 'tpep_pickup_datetime'

Refiltered the data to keep only data points for  Jan 2019

## Methodology 
First tried the benchmark decision tree model to see the model fit.

Then explored to add new features to see if it improves the model fit. The new features I explored including:

Create new features from current data: 

    transaction date is weekday or weekend

    transaction date is holiday or not

Borough information

weather data

After that I explored two new ML model (Random Forest and Gradient Boosting)  with the data including new features. 

Chosed Random forest model and performed further exploration with different parameters
