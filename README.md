# Project 2 - Ames Housing Data and Kaggle Challenge

## Goal of the project
The goal of this project is to develop a model which can effectively predict housing prices based on certain parameters. These parameters have to be decided by the modeller and would need multiple iterations and inputs from various stakeholders. The models developed in this particular exercise is based on either simplistic version or a very mildly features engineered model.

## Dataset
The dataset set used here is Ames Housing dataset. there are two parts in data.One is train.csv and other is test.csv. Train csv has sale prices available while sale prices need to be predicted for test.csv.
The distribution of sale prices is right skewed, hence these values are being log transformed. The training data is not clean. So first the cleaning of this dataset was done,to eventually find no nulls in 2050 entries, certain columns were dropped in this process such as Alley which had to many missing values.

## Material present here
here are two Jupyter notebooks here. One does EDA,Imputation and Linear Regression for the train data namely 'Saba_Project_2_EDA' while the other does basic cleaning of continuous variables in the test column called as 'Saba_project_2_test_data_continuous' the result of which is saved as 'Model_2_continuous.csv'. 
There is a dataset pertaining to the feature engineered model 1 developed in the notebook 1 namely 'Cleaned_Test_Data_for_Prediction.csv'.

Exhaustive cleaning has been done for the 'train.csv' to aid us in building any number of models in the future. 
Scatter plots and other relevant plots have been drawn for all the features against the sale price. 
The results of the various regressions have been saved as csv files namely 'Model_1_SLR.csv','Model_2_SLR.csv', 'Model_ridge.csv','Model_lasso.csv'.

## Models
Models employed are:
1. feature Engineered
2. Linear Regression with continuous variables
3. Ridge Regression with continuous variables
4. Lasso continuous with continuous variables


I have got strange results with extreme over-fitting, which I don't agree with, nevertheless will show them. However I found ridge and lasso giving much better results. 





