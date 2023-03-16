# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
The purpose of analysis is to determine the health of credit loan. The problem to sort is the imbalanced data that can create biases in model. Therefore we use RandomOverSampler to adjust our data in a more effective model.
* Explain what financial information the data was on, and what you needed to predict.
the financial data we use come from lending_data.csv, and we set loan status as our target prediction (y) with the rest as our variable features.  
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
- default loan as our target prediction that we train and test
- loan size, interest rate, borrower income, debt to income, number of accounts, derogatory remarks as our variable to predict
* Describe the stages of the machine learning process you went through as part of this analysis.
first I labelled and set the 'target' and 'feature'. 
then we use train_test_split, before we call the model (logistic_regression) and fit the  training data in.
after that, we produce the prediction through .predict function
from there create the accuracy report, confusion matrix, and classification.
for oversampled data, we  call and fit the training data into RandomOverSampler to equalize the difference between value in y by increasing the number of unhealthy loan. 
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
- LogisticRegression to call the model
- RandomOverSampler to eliminate bias by increasing the minority data
- use balanced_accuracy_score, confusion_matrix, classification_report_imbalanced to find the accurary, precision and recall.
## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
the oversampled data performed slightly better than the original data. We can see it from classification report of original data on '1'or unhealthy loan, that shows 0.91 on recall and 0.85 on precision. 
Eventhough this can be seen good enough for both recall and precision and seemingly perfect for accuracy, the risk of 9% error on recall implying that there is possibility of 1 to 10 that our model classifies high risk loan as low risk loan. This instance is more seriously detrimental than classifying low risk as high risk. 

Our effort and attention should be optimized more on the recall or prioritize to locate high risk loan from the rest. 

If you do not recommend any of the models, please justify your reasoning.

The accuracy of both model is really high and provide a seamless prediction. But uncovering deeper issue and projecting the true results we need to create a robust model, neither models are effective enough to be used in real life. One way to improve the model if the resource (time and money) is limited, is to try improving on finding unhealthy loan (high risk) or focusing in improving recall reports.
