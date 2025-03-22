# Module 12 Report

## Overview of the Analysis

The purpose of the analysis is to create a model that accurately identify the risk of default given a list/table of loan data. 

The crucial fields in training and test data are the loan initial balance, current balance, interest rate, borrower income, missed payments, number of total credit accounts and debt to income ratio. These values are the numerical predictors used to primarily understand if a loan is "healthy" or is "high risk" and may default.

The main output of the model is to label healthy loans as 0 and high risk loans as 1 with the highest accuracy possible. 

This analysis involved 77.5k records, with roughly 57k used for training, and the remaining 20k used for testing the accuracy of the model. For this specific analysis we trained this using a Logistic Regression available via Python libraries, specifically Sklearn. 

## Results

Out of 19384 records tested, these were my results in the confusion matrix:
[18673,    86]
[   32,   593]

    * Precision was 593/(593 + 86) or 87.3%.
    * Recall was was 593/(593 + 32) or 94.88%.
    * Accuracy was 99%. 

## Summary

This model was in my opinion successful at predicting high risk loans. I believe the 99% is slightly misleading given the large number of Healthy Loans versus High Risk loans in our data set. If more loans were defaulting the accuracy score would likely go down slightly but stay above the 90% mark. 

In this instance, a few more false positives are preferable to false negatives. This is simply because we would rather be able to see which loans might default versus have our model miss the defaulting loans which would come as a surpise loss to the bank (false negatives). Ideally all loans would be paid back, and it is possible even the high risk loans are paid off by borrowers, but we would rather "over label" high risk loans slightly in order to reach out to consumers if necessary, identify how much capital to set aside to offset the losses, sell the loans, etc. 

Given that our model has very few false negatives given the number reviewed, I think this is a successful and useable model for identifying possible defaults. 
