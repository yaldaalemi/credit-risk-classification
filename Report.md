# Module 12 Report Template

## Overview of the Analysis

In this section, we will describe the analysis conducted for the machine learning models used in this Challenge. This includes:

- **Purpose of the Analysis**: The purpose of this analysis is to build a model that can identify the creditworthiness of borrowers.

- **Financial Information and Prediction**: The financial information used as features for the model included loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, total debt, and the loan status to be predicted. The goal is to determine whether a loan is healthy or high-risk.

- **Variable Information**: For the 'loan status' variable, there are 75,036 healthy loans and 2,500 high-risk loans. This indicates a significant class imbalance.

- **Machine Learning Process Stages**: The machine learning process involved the following stages:
  1. Setting the 'loan status' column as the target variable (y) and the remaining columns as features (X).
  2. Splitting the data into training and test datasets.
  3. Using a Logistic Regression model for classification.
  4. Training the model on the training dataset.
  5. Testing the model on the test dataset and comparing the predictions to the y_test data.

- **Methods Used**: In addition to splitting and using Logistic Regression, resampling was applied to balance the class sizes. This was necessary because the population of healthy loans significantly outnumbered high-risk loans, and resampling helped improve the model's performance in predicting high-risk loans.

## Results

Here are the results for the machine learning models:

### Machine Learning Model 1

- **Accuracy**: 0.99
  - Note: While accuracy is high, it may not be the best indicator due to class imbalance.
- **Precision**: 100% for healthy loans, 87% for high-risk loans.
- **Recall**: 100% for healthy loans, 100% for high-risk loans.
- **F1-Score**: A balanced measure that considers precision and recall.

### Machine Learning Model 2

- **Accuracy**: 0.99
  - Note: While accuracy is high, it may not be the best indicator due to class imbalance.
- **Precision**: 100% for healthy loans, 87% for high-risk loans.
- **Recall**: 100% for healthy loans, 89% for high-risk loans.

The second model showed improvements in recall for high-risk loans, indicating that resampling the data helped classify all high-risk loans.

## Summary

In summary:

- **Model Recommendation**: Model 2 is preferred due to its improved performance in identifying high-risk loans. However, the choice of model may depend on the organization's priorities.
  
- **Performance Consideration**: The choice between models should consider the organization's goals. If minimizing high-risk loans is the top priority, precision should be emphasized to ensure that only healthy loans are approved. If the goal is to approve as many loans as possible without missing healthy loans, recall becomes more critical to minimize false negatives, even if it means including some high-risk loans. Balancing precision and recall may be necessary in some cases.
