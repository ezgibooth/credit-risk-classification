# credit-risk-classification

## Overview of the Analysis

* The purpose of the analysis is to use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can accurately identify the creditworthiness of borrowers. The data used included information on loan size, interest rate, borrower income, debt to income ration, number of accounts, deragotary marks, total debt and loan status.</br>

* In this classification model, the goal is to predict loan status; whether a loan is health or at risk. This is the dependent variable, y, while the remaining information is used as independent variables (x) to predict loan status. </br>

* For this analysis, the data was split into to parts, training set and test set. For each set, the x and y values were defined. Then, logistic regression model was used to fit and analyze the data in order to make predictions. </br>

* Since the dataset used was inbalanced consisting of 75,036 healthy loans vs. 2,500 high-risk loans, the above described logistic regression classifier was repeated with a resampled training data that was created using the RandomOverSampler module from the imbalanced-learn library. 

## Results

Below is a summary of the results, the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1 - Logistic Regression Model with Initial Data:
![1](https://user-images.githubusercontent.com/118090932/234967436-ff9ee31a-835d-45b9-9ff5-05a1256df428.png)
![2](https://user-images.githubusercontent.com/118090932/234967448-bb7e8dad-72da-46f9-b23f-fa1b03eb0dfc.png)

* Machine Learning Model 2 - Logistic Regression Model Randomly Oversampled Data:
![3](https://user-images.githubusercontent.com/118090932/234967498-05da75fc-c846-478e-be3e-bd8c928b73bd.png)
![4](https://user-images.githubusercontent.com/118090932/234967516-0f5b6407-077a-4738-9068-3f204ade5877.png)

## Summary

The logistic regression model performs well in predicting '0', healthy loans, with a precision score of 100% and accuracy of 99% and a recall score of 99%. These results indicate that the model works well in correctly identifying healthy loans. However, this does not hold true for high-risk loans. The model's precision for correctly predicting '1', high-risk loans, is lower, only at 84%. The recall value is also slightly lower than that of the healthy loans, at 93%. These scores indicate that while the logistic regression model performs very well in predicting healthy loans, it does not perform as well when it comes to predicting high-risk loans. Part of the reason may be due to the imbalance of the target values, as there are 75036 healthy loans versus only 2500 high-risk loans, in this dataset.

The logistic regression model fit with oversampled data has a slightly higher accuracy rate compared to the initial regression model. While performance with predicting healthy loans are equally good, it seems this model fit with oversampled data is better at identifying high-risk loans with a higher recall score.

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
