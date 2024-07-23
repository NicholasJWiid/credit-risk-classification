# credit-risk-classification
## Overview of the Analysis
The purpose of this analysis is to identify the creditworthiness of borrowers, by training and evaluating a Logistic Regression model based on loan risk. The dataset a comprised of historical lending activity from a peer-to-peer lending services company, and includes the following fields: loan size, interest rate, borrower income, debt to income ratio, number of accounts, total debt and loan risk. The loan risk field shows 75036 borrowes with low risk and 2500 borrowers with high risk.

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

    * Precision: The occurance of healthy loans (0) shows a value of 1 for precision. This indicates that there a very small % of false negatives in the results. The occurance of high risk loans (1) achieves a precision value of 0.84, also relatively high, but significantly less than healthy loans. The decrease can be attributed to a low overall model balance and higher number fo false postives compared to false negatives.
     
    * Recall: The occurance of healthy loans results in a recall value of 0.99, slightly lower than the healthy loan precision due to small number of false postives in the results. High risk loans acheive a recall value of 0.94, higher than the precision for this class due to the lower number of false negatives in the results.
    
* Additional Machine Learning Model Results:

The results of running several other ML models are as follows.

Model: ExtraTreesClassifier -    Score: 0.991, "0" PRE: 0.995, "0" RE: 0.996, "1" PRE: 0.871, "1" RE: 0.846
Model: BaggingClassifier -       Score: 0.991, "0" PRE: 0.995, "0" RE: 0.996, "1" PRE: 0.893, "1" RE: 0.848
Model: RandomForestClassifier -  Score: 0.992, "0" PRE: 0.995, "0" RE: 0.997, "1" PRE: 0.897, "1" RE: 0.847
Model: KNeighborsClassifier -    Score: 0.992, "0" PRE: 0.994, "0" RE: 0.998, "1" PRE: 0.929, "1" RE: 0.842
Model: AdaBoostClassifier -      Score: 0.994, "0" PRE: 0.994, "0" RE: 1.000, "1" PRE: 0.994, "1" RE: 0.842
Model: AdaBoostClassifier2 -     Score: 0.994, "0" PRE: 0.994, "0" RE: 1.000, "1" PRE: 0.994, "1" RE: 0.842



## Summary

For the Logistics Regression Model there are a very small % of people with a high risk of default that have been classified incorrectly (False Negatives), and only a marginally higher number with a healthy credit record that have been misclassified as high risk by the prediction (False Positives). What is more important is the false negatives, because this has greater negative implications for the bank. The bank it ultimately trying to limit the number of borrowers that end up defaulting even though they were predicted not to, so no action taken under the belief that a borrower will not default has worse implications for bank revenue if they end up defaulting. In contrast, action taken to prevent defaulting for borrowers falsely identified as high risk, does not have the same negative impact since these borrowers won't end up defaulting in reality. In this case, it is more important to predict the 1's accurately.

Including the results of the additional models, it appears that the AdaBoostClassifier2 model works best to get the highest accuracy scores as well as precision for both healthy loans (0) and high risk loans (1). Falas positives are significantly reduced. This is true for recall for healthy loans too, however, recall for high risk loans for this model appears to decrease slightly to 0.842, due to a slight increase in false negatives compared to the other models.

Overall, I would recommend these model be tested further with more data and with additional modelling to balance the data. 
