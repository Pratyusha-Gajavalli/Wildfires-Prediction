# Wildfires-Prediction
1. Introduction and Objective
3. Data Dictionary
4. Data Pre-processing
5. Feature Engineering
6. Model Development
7. Results

#Introduction
Due to global warming, wildfires have become more frequent. This elevates the importance of prediction of wildfires. Objective of this project is predicting frequency of wildfires to a forest, which helps in better management of resources and reduce the effect of disaster. 

#Data Sources and Data Dictionary
1. Train.csv - This file consists of wildfires frequency along with the date it happened and the reporting unit

2. InyoNationalForest.nc - This file is the weather data which consists of the following attributes
    i.Precipitation
    ii.Temperature
    iii.Soil level moisture

#Data Understanding
    i. The frequency of wildfires are following a bell shaped distribution
02

    ii. The trend in the average number of wildfires is varying a lot and is mostly random
03

#Feature Engineering
    i.Features are generated from the weather dataset
    ii.It is highly likely to cause the wildfire when the weather conditions are extreme
    iii.Therefore, Features which can capture the edge cases are being generated. Examples of such features are Max, Min and Mean of corresponsing weather variables
    iv.Below is the correlation matrix of the variables in the final dataset
04

#Model Development
Model development is an iterative process. The predictor variable is continuous and the following approaches are being tested for prediction modelling 
i.Linear Regression
ii.CAT Boost Regression 
iii. Random Forest Regressor 
##Linear Regression
i. It is clear from the correlation matrix that most of the variables are auto correlated which violates the assumption of Linear regression
ii.Therefore, Variance Inflation factor (Linear relationship between the one independent variable and other independent varibles) is being checked and established a cutoff of 7
iii. Even though, Variables are being removed in every iteration due to multicollinearity, the accuracy of the model isn't varying much 
iv. The final model can be called as "Parsimonious model" with only Pev_max, month indicator and tp_min variables 
##CAT Boost algorithm
i.One of the main reasons to choose CAT boost is that it can perform well even if the data is less 
ii.Also, since the month is a categorical variable, using CAT boost can be more beneficial 
##Random Forest Regressor
i.One of the main reasons to choose CAT boost is that it can perform well even if the data is less <br>
ii.Also, since the month is a categorical variable, using CAT boost can be more beneficial     
#Results
1. Linear Regression performed much better than the other non linear advanced algorithms
2. With increase in pev_max, there is an decrease in the number of wildfires 
3. The increase in tp directly corresponds to the increase in the number of wildfires 
#Future Steps
1. More variables which can impact Wildfires can be included in the model 
2. Time series forecasting can also be done to predict the number of Wildfires
3. It will be very interesting to see the real effects of important variables on Wildfires
#Thank You!
