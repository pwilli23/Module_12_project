# Module 12 Report Template

## Overview of the Analysis

* What is the purpose of the analysis?:
The purpose of the analysis is to identify the creditworthiness of borrowers 
* What financial information the data was on, and what you needed to predict.
The financial data of potential loanees provided in the report were: desired loan amount, interest rate, borrower income, debit to income ratio, number of accounts, total debt, and loan status
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).

We were trying to predict whether a loan was healthy or if it was a high-risk loan with 0 representing a healthy loan and 1 representing high-risk loans

* Describe the stages of the machine learning process you went through as part of this analysis.
## Stage 1: Setting up the Machine Learning Process:

* Step 1: We first had to separate the data into labels and features features were created by select the loan_status column of the loan_df DataFrame. Labels were created by dropping the loan_status column from the loan_df DataFrame

* Step 2: Checked the balance of the label variable y by using `value_counts()` and split the Data into training and testing datasets by using `train_test_split`

* Step 3: Fit a regression model by using the trained data `X_train` and `y_train` and saved the predictions on the testing data labels by using `X_test` and the fitted model 

## Stage 2: Evaluate the Models Peformance:

* Step 1: Checked the balanced accuracy score of the model using the `balanced_accuracy_score` function

* Step 2: Generated a confusion matrix for the model to see by the numbers how accurate our model was: `confusion_matrix`

* Step 3: Printed the classification report for the model using the `classification_report_imbalance()` function. 

## The Resampling Method: 

### Stage 1: Use the Resampled Data and the LogisticRegression classifier to fit a new model to make predictions:

* Step 1: Use the `RandomOverSampler` function to set the `random_state` to 1 

* Step 2: Fit the original training data to the random_oversampler model by using the `fit_resample` function

* Step 3: Use the `LogisticRegression` function to fit the model and make predictions

### Stage 2: Evaluate the Models Performance:

* Check for the same statistics as in model 1

## Results

### Machine Learning Model 1:

* Model 1 had a 93.935% balanced accuracy score

* The model's precision for healthy loans was close to 100% while the precision identifying high-risk loans was 86%

* The model's recall for healthy loans was also close to 100% while the recall for high-risk loans was 91%
### Machine Learning Model 2:

* Model 2 had a 99.3% balanced accuracy score 

* The model's precision for healthly loans was close to 100% while the precision for high-risk loans was 84% 

* The model's recall for healthy loans was 99% while the recall for high-risk loans was 99%

## Summary

* In conclusion, Model 2 outperformed Model 1 because it more precisely identified and predicted the high-risk loans.  It is While it was slightly less accurate predicting and identifying healthy loans, its ability to identify those borrowers who are likely to default on a loan was signifcantly better.  It is more important for the credit union to better identify high-risk borrowers than it is to lend out more money to those who are less likely to pay back.   
