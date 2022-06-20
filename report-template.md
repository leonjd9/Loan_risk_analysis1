# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
-The porpuse of the analysis is to compare the performace of two predicting model, one using the original data and the other applying oversampling techniques that allow the model to balance the amount of postive and negative results.

* Explain what financial information the data was on, and what you needed to predict.
The data had a list of loan data with different multiple dimensions including the staus of the loan(healthy or on default). This study will provide the financial company with valuable infomation about which type of characterisitcs manifest on healthy borrowers and the ones that then to default.

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
With this function, I was trying to reveal how balanced the data presented is. In this case the number of defaulted loans was substantially low compared to the healthy loans. Consequently, the model will present a low sensitivity to defaulted loans.
* Describe the stages of the machine learning process you went through as part of this analysis.
The machine learning process consists of first, preparing the data(isolating the the y and the X). Subsequently, we train and split the data using the sklearn train_test_split function. Then we fit a logostic regression model with a random state of 1. Then, we proceed to run our predictions using the models created and analysis the results with confusion matrix, accuracy and classificaiton fucntions.

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
 -Model one shows an accuracy of 99.21 yet we need to consider we are workign with unbalanced data. The precision for healthy loans is 100% and for default is 86%. Recall for "0" is also 100% and 90% for "1".


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
 -Resampled model shows an accuracy of 99.61%(higher than original model). The precision for healthy loans is 100% and for default is 84%. Recall for "0" is also 99% and 2000% for "1".

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

The resampled model works best becasue the opriginal is highly influeced by the overwhelming amount of healthy loans. This results in unrealistic high accuracy and precision scores for the healthy loans which can be costly for the financial company. I would reccomend the resampled model for further development.


If you do not recommend any of the models, please justify your reasoning.
