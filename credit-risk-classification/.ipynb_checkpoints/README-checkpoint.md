# Credit Risk Analysis Report
## Overview of the Analysis

The purpose of this analysis is to build a machine learning model that can predict the creditworthiness of borrowers. By analyzing historical lending activity data, we aim to develop a model that can accurately identify healthy loans (0) and high-risk loans (1). Each model's performance could be evaluated using various metrics, including accuracy, precision, and recall. (Please see .ipynb file in this repository)

## Results
The results of the machine learning model with the original data are as follows:

* Accuracy Score: 95.20%
* Precision Score: 85%
* Recall Score: 91%
* F1-Score: 88%

The results of the machine learning model with the randomly balanced data are as follows:

* Accuracy Score: 99.37%
* Precision Score: 84%
* Recall Score: 99%
* F1-Score: 91%

## Summary

Based on the evaluation metrics, we have compared the performance of two machine learning models for credit risk classification: the logistic regression model using the original data and the logistic regression model with resampled training data.

The logistic regression model with the original data achieved an accuracy score of 95%. It demonstrated 85% precision and 91% recall when classifying high-risk loans. These results indicate a strong performance overall, however the caviat is dealing with the imbalance within the data provided. Therefore a more accurate measure for this model is our F1-score of 88%.

On the other hand, the logistic regression model with resampled training data produced an accuracy score of 99% just like the first model. However, it exhibited a slightly weaker precision of 84% and a significantly stronger recall of 91%. This model's performance suggests that it is more adverse to classifying  healthy loans as high-risk and overall classifies applicants more accurately. This is also reflected in the stronger F1-score of 91%.

When comparing the two models, it would be best to compare the F1-scores because it tries to eleminate bias when comparing datasets with imbalances to one another. Therefore, based on these metrics, the second model would most likely be the better choice depending on what the cost of misclassifying a high-risk as healthy.

Consideration should be given to the specific requirements and business objectives when selecting a model for credit risk classification. If it is significantly more costly to misclassify high-risk loans as healthy, we may recommend using first model because of it is less likely to approve a high-risk applicant. However, if the weighted cost of falsely classified healthy loan as high-risk out weighs the amount of high-risk misclassifications, the second model would be the best option.