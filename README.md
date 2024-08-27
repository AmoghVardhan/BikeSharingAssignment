# BikeSharingAssignment

## Problem Statement
A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state.

## Process
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
For achieving maximum bookings, the features with higher coefficients needs to be given more importance
- if temp increases, cnt increases
- if it is season_4 (winter), cnt increases
- if humidity, windspeed decreases, cnt increases (since coefficient is negative)
- if weather is mist or light snow, the cnt decreases (since coefficient is negative)
