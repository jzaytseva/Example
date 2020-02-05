# Project 2 - Ames Housing Data and Kaggle Challenge

## Content:
**1. Exploratory Data Analysis (EDA)**:
   - Import Packages and Data
   - High Level Checks
   - Investigating Target Variable (SalePrice)
   - Investigating Features: Univariate Distribution
   - Bivariate Analysis
   - Handling Outliers
   - Data Cleaning
   - Checking Missing Values
   - Imputing Missing Values
   - Store Clean Data

**2. Feature Engineering:**
   - Exploratory Visualizations
   - Dummy Variables Creation
   - Automatic Log Feature Selection
   - Revisiting Exploratory Data Analysis: Correlations Deep Dive
   - Preprocessing
   - Determine Baseline Score
   - Linear Regression

**3. Model Tuning:**
   - Train/Test Split Train data
   - Scaling/Normalization
   - Cross Validation
   - Benchmark Modeling - LASSO Regression with All Features

**4. Production Model and Insights**
   - Model
   - Ridge VS Lasso
   - Metrics
   - Kaggle Sumbission
   - **Conclusion**


## Problem Statement

   I am interested in real estate market and believe it maybe one of the easiest and fastest way to earn money. Also, it involves a lot of risk. There many features that are involved in house sales and these features impact the sale price dramatically. Using dataset of Ames, Iowa housing I will investigate sale price and study features that will help to predict the final sale price. I examined this question from prospective of an investor and a house owner: **what should I look at to increase  ROI (from buying or selling) a  house in Iowa?**

To answer that question, we have explored a large data set of over 2000 homes and used that insight to build a predictive linear regression model.

## Datasets
The data set utilized were:

- [Train.csv](https://git.generalassemb.ly/jzaytseva/project_2/blob/master/datasets/train.csv) is the primary dataset used for the project.The train.csv dataset contains all the housing features to explore, including the sales price, which is our target variable.

- [Test.csv]( https://git.generalassemb.ly/jzaytseva/project_2/blob/master/datasets/test.csv) dataset is included for validation purposes. This is the file upon which I will make my conclusion. It does not have the 'SalePrice' column. The purpose of this project is to generate a model that can be tested with test.csv to see how closely the predictions match prices on unseen data.

## Data Dictionary :
- [Data description](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt)

## Executive Summary

I started by exploring and understanding the dataset.The training set contains 1095 observations and 81 variables. Based on the initial observation I divided our variables into categories: Continuous, Categorical, Numerical, Nominal and Target variables. 

**Sale price** is the value I was looking to predict in our project, so it made sense to examine this variable first.  The sale price exhibited a right-skewed distribution that was standardized in the training data in order to create a good model. Once it was done, I was no longer violating the normality assumption for regressions. 

Next step was to deal with missing data in order to pick the best features to include in my model. But before I needed to find out relationship between my target variable (SalePrice) and potential predictors. After I established relationship using numerical and categorical variables I could proceed with cleaning and don't worry to exclude variables that have no effect at the sale price. This began with figuring out which columns had null values and deciding what to do with the nulls. After cleaning the data came visualizing the relationship between the different variables and sales price. Outliers were identified and feature engineering of columns were applied. By eliminating outliers and adding new variables to provide enriched information to our model I ensured that all necessary features of the data will be represented during modeling process. 
After choosing the features for my model, I created 3 different models, linear regression, ridge and LASSO. The models were evaluated using different metrics and conclusions and recommendations were successfully obtained to answer our problem statement.



## Conclusion and Recommendations

I wanted to engineer features that will help to predict sale price of houses in more accurate way and help sellers and buyers in decision making process. I identified factors that influence on price such as location , square footage and even garage. Also I created features to better understand classification of expenses.
*For example: for a studio, which is 'X' square feet the price is "$$ . *However the price is doubled for the same size 'X' sqft which is named 1 bedroom.*

Based on my Ridge model, the top features that influence the value of a home are:  **Overall Quality** and **Gr Liv Area**. Ridge perfomed better on the traing set and captured the variance in actual Sale price. Our model is overfitted. However, using Lasso model we can see the Testing  𝑅2  is 0.041 lower than the Training  𝑅2. Overall, Ridge model was the best that handled unseen data.

Also I took a look at location of cheapest and most expensive houses. According my analysis, certain neighborhoods have benefits, they also come with their own negatives. For cheaper neighborhoods, while their remodeling rate was much higher than those of expensive ones, there is also the risk of being unable to gain a large ROI as all the other homes in the area are priced lower. With the expensive neighborhood, you run the risk of not being able to remodel enough to get a greater ROI. Also, as home prices in that area are more expensive, the price tag might make it harder to sell as quickly as possible.


Given all of this information, it will be useful to look into each neighborhood and change specific qualities of homes to see its predicted price. I would recommend to add to this research schools and gyms and take them into consideration as well. The model will be useful for being able to estimate house prices from a one unit change in certain features. It can estimate the ROI and isolate which houses have the most potential for remodeling.

Taking timing into account, I would add housing market crises as one of criteria to this research. It has obvious affect on our datasets and impact prediction of on sale price. This model was built **strictly**  for the Ames home market. Additionally, I wouldn’t recommend to apply it. Based on my analysis, there are a lot of missing data, quality of given information is low, and to build accurate model needs more time and more related information.


## Presentation can be found here [presentation]( https://git.generalassemb.ly/jzaytseva/project_2/blob/master/Presentation%202.pptx) 
