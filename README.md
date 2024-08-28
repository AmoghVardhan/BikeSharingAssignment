# BikeSharingAssignment

## Problem Statement
A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state.

## Process
We are choosing a multiple linear regression approach to solve this problem. Once the model is built, residual analysis is done to confirm that our assumptions are valid for this data.
-	Load data from the csv file
-	Pre-processing of data (check data types, null values, outliers, derived variables)
-	EDA ( analyse the feature variables to better understand the data we are going to model)
-	Handling categorical features using one hot encoding
-	Scaling of features so that the coefficients are interpretable and also for faster convergence of the gradient descent algorithm.
-	Feature selection using RFE & modelling using sklearn and statsmodel library to drop features which have high p value (> 0.05) or high VIF ( > 5)
-	Residual analysis to test if the error terms are normally distributed to validate that our assumption is correct
-	Model interpretation by checking which feature positively or negatively affects the target variable by interpreting the coefficients

## Model Results
Final Result Comparison
- r2 Train: 0.841 
- r2 Test: 0.805
- adjusted r2 train: 0.836 
- adjusted r2 test: 0.79
The model with r2 test > 0.8 is a good model fit.

## Inference
The model equation:

cnt = 0.23*const + 0.54*temp - 0.18*hum - 0.18*windspeed + 0.10*season_2 + 0.14*season_4 + 0.23*yr_1 + 0.05*mnth_8 + 0.12*mnth_9 - 0.10*holiday_1 - 0.054*weathersit_2 - 0.24*weathersit_3

Top 3 features are:
- Temp => a unit increase in temperature, increases the bike demand by 0.54
- Weathersit_3 (Light snow, light rain+ thunderstorm) => a unit increase in weathersit_3, decreases the bike demand by 0.24
- Yr_1 (the year 2019) => if the year is 2019, the bike demand increases by 0.23
