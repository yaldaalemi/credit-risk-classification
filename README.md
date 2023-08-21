# Credit Risk Classification Analysis

## Overview

In this project, I conducted an analysis of credit risk classification using various machine learning techniques. The goal was to build a model that can accurately identify the creditworthiness of borrowers. I used a dataset of historical lending activity from a peer-to-peer lending services company to train and evaluate the model.

## Steps Taken

### 1. Data Preparation

- Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.
- Created the labels set (y) from the "loan_status" column.
- Created the features (X) DataFrame from the remaining columns.

### 2. Data Splitting

- Split the data into training and testing datasets using the `train_test_split` function.

### 3. Model Building

- Utilized logistic regression to build a predictive model.

### 4. Model Modification

- Applied resampling to balance the class sizes for the second model and improved the model's performance in predicting high-risk loans.

### 5. Model Evaluation

- To see the results of the model evaluation and the detailed analysis, please refer to the report file.
