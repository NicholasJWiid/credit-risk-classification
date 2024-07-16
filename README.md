# credit-risk-classification
## Overview of the Analysis
The purpose of this analysis is to identify the creditworthiness of borrowers, by training and evaluating a Logistic Regression model based on loan risk. The dataset a comprised of historical lending activity from a peer-to-peer lending services company, and includes the following fields: loan size, interest rate, borrower income, debt to income ratio,	number of accounts, total debt and loan risk. The loan risk field shows 75036 borrowes with low risk and 2500 borrowers with high risk.

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
* Machine Learning Logistic Regression Model Results:
    * Accuracy: The overall accuracy score is high, showing 0.99, indicating that the model is highly accurate.

    * Precision: The occurance of healthy loans (0) shows a value of 1 for precision. This indicates that there a very small % of false negatives in the results. The occurance of high risk loans (1) achieves a precision value of 0.84, also relatively high, but significantly less than healthy loans. The decrease can be attributed to a low overall model balance and higher number fo False postives compared to false negatives.
     
    * Recall: The occurance of healthy loans results in a recall value of 0.99, slightly lower than the healthy loan precision due to small number of fasle postives in the results. High risk loans acheive a recall value of 0.94, higher than the precision for this class due to the lower number of False negatives int he results.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.


Overall, this means that there are a very small % of people with a high risk of default that have been classified incorrectly (False Negatives), and only a marginally higher number with a healthy credit record that have been misclassified as high risk by the prediction (False Positives). What is more important is the false negatives, becasue this has greater negative implications for the bank. The bank it ultimately trying to limit the number of borrowers that end up defaulting even though they were predicted not to, so no action taken under the belief that a borrower will not default has worse implications for bank revenue if they end up defaulting. In contrast, action taken to prevent defaulting for borrowers falsely identified as high risk, does not have the same negative impact since these borrowers won't end up defaulting in reality. In this case, it is more important to predict the 1's accurately.

I would recommend the model be tested further with more data and additional modelling is done to balance the data.






