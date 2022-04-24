# Module 12 Report

## Overview of the Analysis

* What is the purpose of the analysis?:
The purpose of this project is to create a trading algorithm model that tells a user when to buy or sell an asset.  
* Overview of the Project:
In this project we created 3 different algorithmic trading bots to find the optimal trading strategy.  The first model was created as a baseline model, the second model slightly altered the input parameters to improve the models accuracy. The third model was a Logistic Regression model and was used to compare its accuracy to the first 2.  

* Describe the stages of the machine learning process you went through as part of this analysis.
## Stage 1: Establishing Baseline Performance:

* Step 1: We first had to import the OHLCV data and used the `pct_change` function on the closing price data to generate our `Actual Returns` data

* Step 2: Generated trading signals using short and long window SMA values

* Step 3: Created a Signal column that indicated whether the user should buy or sell stock based on whether Actual Returns are greater or less than 0. 

* Step 4: Added a "Strategy Returns" column to the DataFrame and set its value equal to `'Actual Returns' * 'Signal'` 

* Step 5: Created our training and testing daya by using the SMA Fast and SMA Slow as our X value and our 'Signal' column as our y value

 
