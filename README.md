# credit-risk-classification
## Overview of the Analysis
The purpose of this analysis was to identify the creditworthiness of borrowers, by training and evaluating a Logistic Regression model based on loan risk. The dataset a comprised of historical lending activity from a peer-to-peer lending services company, and includes the following fields: loan size, interest rate, 	borrower income, debt to income ratio,	number of accounts, total debt and loan risk. The loan risk field shows 75036 borrowes with low risk and 2500 borrowers with high risk.

### Description of chosen method: Logistics Regression
Logistics Regression is a statistical method of classification used to predict the binary outcomes from data. Predicted outcomes are then evaluated against the actual outcomes in order to assess the accuracy of the model and the ability of the model to then be recommended for further use.

### Machine Learning Steps
1. Reading in the data and seperating it into labels and features.
2. Splitting the data into two datasets: Training data and Testing data.
3. Setting up the Logistic Regression model and fitting the Training data.
4. Making predictions with the trained model using the Test feature data.
5. Comparing the label predictions with the actual label values using a confusion matrix.
6. Creating a classification report to look at the precision, recall and f1-score.

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Logistic Regression Model:
    * Accuracy:

    * Precision:
     
    * Recall:

The logistic regression model predicts the occurance of healthy loans (0) with a high degree of accuracy, achieving a value of 1 for precision and 0.99 for recall. The prediction for the occurance of high risk loans (1) is still quite strong but weaker than the prediction of healthy loans, with the classification of high risk loans reporting a precision of 0.84 and a recall of 0.94 respectively. 

Overall, this means that there are a very small % of people with a high risk of default that have been classified incorrectly (False Negatives), and only a marginally higher number with a healthy credit record that have been misclassified as high risk by the prediction (False Positives).

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.






