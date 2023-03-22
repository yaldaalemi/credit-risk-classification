# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* The purpose of the analysis is to build a model that can identify the creditworthiness of borrowers.
* Explain what financial information the data was on, and what you needed to predict.
* The financial information that were provided to the model as features were the loan size, the interest rate, the borrower income, the debt to income ratio, number of accounts, derogatory marks and the total debt and the loan statu was to be predicted and determined if it was a healthy loan or a high-rist loan. 
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* The value counts for the loan statu showed 75036 for healthy loans and 2500 for high-risk loans. which means that the population of the healthy loans was almost 30 times the population of the high-risk loans. 
* Describe the stages of the machine learning process you went through as part of this analysis.
* The first step was to set the loan statu column as y and the rest of the columns as X. Then the data was split to training and test data sets. After instantiating the Logistic Regression model the training data set was fit to the model to train the model and after that the model was tested by using the test data set and comparing the predictions to the y_test data set.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
* Except splitting the data, and using LogisticRegression model to classify the data and predict the outcome, resampling was used. Since as mentioned earlier, the population of the healthy loans was almost 30 times the population of the high-risk loans, the data was resampled to have an equal size of both populations and after resampling each had 56277 samples on it and it improved the model in predicting the high-risk loans. 
## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
* The accuracy of the model is 0.99 which means that the model is correct 99% of the time but it is not a good indicator to evaluate the model with since in this case for example, the healthy loans outweight the high-risk loans. It is better to evaluate the model by the other indicators shown in the classificatino report. Precision is the ratio of correctly predicted positive observations to the total predicted positive observations which means that out of all the loans classified as healthy loans 100% of them are healthy loans but out of the loans classified as high-risk loans only 87% are actually high-risk loans and 13% are false positives. Recall is the ratio of correctly predicted positive observations to all predicted observations for that class. This means that out of all the healthy loans 100% of them were classified correctly as healthy loans but out of all the hight-risk loans, 89% of them were calssified correctly as high-risk loans. F1-score takes into account both the precision and the recall and we can conclude that overall the model is much better at predicting the healthy loans compared to high-risk loans.



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
 * The healthy loan prediction did not have any room for improvements since precision and recall were already 100%. The precision for high-risk loans has stayed the same but the recall has improved from 89% to 100%. Meaning that resampling the data helps to classify and identify all of the high-risk loans despite the first model.  

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

The second model is better but overall it depends on the priority of the organization. If the goal is to minimize approving the high-risk loans, then the precision is more important to insure that the model only approves the healthy loans. On the other hand, if the goal is to approve as many loans as possible without missing any healthy loans, then the recall is more important to make sure that the model does not miss any healthy loans even though it might include some high-risk loans. In some cases a balance between the precision and the recall is needed. 
