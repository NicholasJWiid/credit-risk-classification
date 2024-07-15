# credit-risk-classification
## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).


The purpose of this analysis was to identify the creditworthiness of borrowers, by training and evaluating a Logistic Regression model based on loan risk. The dataset a comprised of historical lending activity from a peer-to-peer lending services company, and included the following fields: loan size, interest rate, 	borrower income, debt to income ratio,	number of accounts, total debt and loan risk. The loan risk field included some 75036 borrowes with low risk and 2500 borrowers with high risk.

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.






The logistic regression model predicts the occurance of healthy loans (0) with a high degree of accuracy, achieving a value of 1 for precision and 0.99 for recall. The prediction for the occurance of high risk loans (1) is still quite strong but weaker than the prediction of healthy loans, with the classification of high risk loans reporting a precision of 0.84 and a recall of 0.94 respectively. 

Overall, this means that there are a very small % of people with a high risk of default that have been classified incorrectly (False Negatives), and only a marginally higher number with a healthy credit record that have been misclassified by the prediction to be high risk (False Positives).