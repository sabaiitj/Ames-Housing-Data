# Project 2 - Ames Housing Data and Kaggle Challenge

## Problem Statement
Primary objective of the project is to predict sale prices of the house for the sellers and prospective buyers to optimize the house buying process. The goals of this project are following:
* Analyze the provided dataset,
* Understand the relationship between different features through EDA, 
* clean the data through deletion and imputing the data
* Creating graphs to visually understand the relationship between features.
* Develop a regression model which can effectively predict housing prices based on certain parameters. 


## Provided Dataset
The dataset set used here is Ames Housing dataset. There are two parts in data. 
* train.csv: This is the input training data, already has sale price of the house and requires cleaning
* test.csv: This is the input test data which requires cleaning and needs the housing price prediction.
 

**Note:** The distribution of sale prices is right skewed, hence these values are being log transformed. The training data is not clean. So first the cleaning of this dataset was done,to eventually find no nulls in 2050 entries, certain columns were dropped in this process such as Alley which had to many missing values.

## Output
As part oif the project, I have produced multiple artifacts. 
* Jupyter Notebooks
*  1. Saba_Project_2_EDA: EDA, Imputation and Linear Regression for the train data. 
*  2. Saba_project_2_test_data_continuous: This does basic cleaning of continuous variables in the test column, the result is saved in `Model_2_continuous.csv`
*  DataSet including results of various regressions:
   *  `Cleaned_Test_Data_for_Prediction`: dataset pertaining to the feature engineered model 1 developed in the notebook `Saba_Project_2_EDA`.
   *  `Model_2_continuous`: dataset pertaining to the feature engineered model 1 developed in the notebook `Saba_project_2_test_data_continuous`.
   *  `Model_1_SLR.csv`: Feature Engineered Model 
   *  `Model_2_SLR.csv`: Linear Regression with only continuos variables Model
   *  `Model_ridge.csv`: Ridge Model
   *  `Model_lasso.csv`: Lasso Model
 
Exhaustive cleaning has been done for the 'train.csv' to aid us in building any number of models in the future. I have dropped any column which has more than 50% missing values and used interpolation & imputation to drive the values for the rest missing row values.  
Scatter plots and other relevant plots have been drawn for all the features against the sale price to visually understand the relationship between a column and sale price of the house.

Identify and bucketize the columns into different datatypes ['nominal', 'ordinal', 'discrete', 'continuos']


## Models
Models employed are:
1. Feature Engineered
2. Linear Regression with continuous variables
3. Ridge Regression with continuous variables
4. Lasso continuous with continuous variables

## Conclusion
I have got strange results with extreme over-fitting, which I don't agree with, nevertheless will show them. However I found ridge and lasso giving much better results. 





