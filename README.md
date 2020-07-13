# Regression-Model-for-House-Pricing-Prediction

Ames, Housing Model

Problem Statement

To predict house pricing in Ames, Iowa for house buyers and sellers by analyzing qualitative and quantitative features by creating a regression model.

Executive Summary

Overview

Kaggle which is an online community of data scientists and machine learning apprentices have shared the Ames Housing Dataset which has 81 columns of different house features.This dataset consists of 39 quantitave features and 42 qualitative features which will be analyzed by category. This model will make predictions of the house pricing by analyzing in detail both feature groups and their correlation between the sale price.

Content

-Dataset Cleaning

-Exploratory Data Analysis

-Data Visualization

-Pre-processing

-Feature Engineering

-Modeling

-Evaluation of the Model

-Conclusions and recommendations

Analysis and Modeling

Initially the features were evaluated with the data library to see their specific representation and categories. . After being familiarized with the features, the cleaning of the dataframes began by checking the types of each column or feature to see if they were correct and making the change to their correct types.

This dataset contained null values, by observing the data library there were some houses for example, that didn't have pool or other features. Regarding to this, 3 approaches were taken by looking at the library and plotting the percentage of null values per column.

1) Some columns with high null values were drop. 2) The quantitative columns were fill with the mean of that specific column. 3) The qualitative columns were fill with the mode of that specific column.

Having these parameters fixed, the data exploratory analysis started by plotting a heatmap which helped to point the correlations between each feature and the saleprice. Eleven quantitative features had a correlation greater than a 0.50, these were taken into further analysis by pair plotting them with the sale price. Scatter plots were analyzed to see if there were outliers that had to be removed and histograms showed how was the distribution among the features and our y = sale price. Some features had outliers and some features were skew.

Following the steps mentioned before, the feature engineering took place by analyzing the high correlated features and combining them for creating columns to improve the normal distribution. This was observed by creating histograms, some combinations didn't get better, so they weren't add to the data frame.

As a next step the categorical feature analysis began, for this boxplots were created to see their mean, outliers, the amount of subcategories in those columns to take the decision with which features were going to be created as dummies. Four features were dummify applying a 0 for False or a 1 for True; the other categorical columns were removed from the dataframe.

After finishing the exploratory data analysis, the data visualization, the pre-processing and the feature engineering; the data was ready fo modeling. As a first step, matrix "X" and target vector "y" were created; "X" consisted in the predictors (features) and the "y" in the prediction = sale price. For "X" 39 features were consider. Then the train test and split was done and the data was scale using the standard scalar; this ir a very important step to do because the features have different scales that can shoot the data.

The model of this project is a linear regression, the model was instantiated and fitted. Different metrics were analyzed like the R2 scores, crossvalidation, coefficients, etc. The model was also regularize using OLS and Ridge.

Conclusions and next steps

There are specific quantitative and qualitative predictors that affect the sale price more than others.

The scores before and after regularization are very similar and consistent the train data had an R2 of 0.87 and for the test data an R2: 0.88.

The R2 scores without and with regularizations were almost the same.

Using the model coefficients per feature can help the house sellers to observe the pricing per feature and obtain more profit from it.

Using the model coefficients per feature can help the house buyers to observe the pricing per feature according to their dream home and budget.

Apply Lasso regularization.
