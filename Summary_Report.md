# Module 12 Report Template

## Overview of the Analysis

#### In this section, describe the analysis you completed for the machine learning models used in this Challenge. 

Explain the purpose of the analysis.Explain what financial information the data was on, and what you needed to predict and provide basic information about the variables you were trying to predict (e.g., `value_counts`). Describe the stages of the machine learning process you went through as part of this analysis and briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

#### The purpose of this analysis was to evaluate the accuracy of logistic regrssion models that predict the creditworthiness of borrows. For the analysis, we used historical lending activity from peer-to-peer lending services to predict whether a potential loan would be healthy (0) or high risk (1). The dataset used contained 77,536 data points and were split into a training and testing dataset. The training dataset was used to create a logisitc regression model which was then applied to the testing dataset. Together the data was used to predict whether the borrowers in the dataset would have healthy/low risk or high risk loan statuses. 


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

####
* Balanced accuracy is used to evaluate the performance of a classifier when the datasets are imbalanced. In this case there are more instances of healthy loans rather than high risk loans. The balanced accuracy provides a more accurate measure of the classifier's performance across all classes, giving equal importance to each class.

* Precision: Precision is the ratio of correctly predicted positive observations to the total predicted positive observations. 

* Recall(sensitivity): Recall is the ratio of correctly predicted positive observations to the all obervations in actual class. It measures the ability of the classifier to final all the positive samples. 

* The macro avg is the average values of precision, recall, and F1-score. 

### Machine Learning Model 1: Description of Model 1 Accuracy, Precision, and Recall scores.
##### 
*Balanced accuracy: 95.2%. The model provides 95.2% accuracy in overall preformance of the classifer across both clases (healthy and risky loans).

*Precision: 92%. The model correctly predicts positive observations in both datasets. It predicts healthy loans with 100% precision and risky loans with 85% precision.  

*Recall: 95%. The model was 95% accurate in predicting the true positive values out of all the predicted positive values. 


### Machine Learning Model 2: Description of Model 2 Accuracy, Precision, and Recall scores.
#### 
*Balanced accuracy: 99.3%. The model provides 99.3% accuracy in overall preformance of the classifer across both clases (healthy and risky loans).

*Precision: 92%. The model correctly predicts positive observations in both datasets. It predicts healthy loans with 100% precision and risky loans with 84% precision.  

*Recall: 99%. The model was 99% accurate in predicting the true positive values out of all the predicted positive values. 


## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

### 
For this analysis, a lending company will want to create a model that classifies healthy and high risk loans correctly based off historical data. Low risk loans that are classifed as high risk loans may drive potential borrows away, however, high risk loans that are classifed as low risk loans may be costly for the lenders if borrowers are unable to pay the loans. 

- True positives occur when model correctly predicts healthy loans. 
- False positives occur when the model classifes as healthy loan as a high risk loan.
- False negatives occur when the model classifes a high risk loan as a healthy loan.
- True negatives occur when the model correctly predicts high risk loans.


####
Model 1 - Unbalanced Confusion Matrix: 
- True Positives: 18,663
- *False Positives: 102*
- *False Negatives: 56*
- True Negatives: 563


Model 2 - Oversampled Balanced Confusion Matrix: 
- True Positives: 18,639
- *False Positives: 116*
- *False Negatives: 4*
- True Negatives: 615

### 
After running the analysis on the unbalanced data model (model 1) and the oversampled balanced data model (model 2), I would advise the lending company to make loan status predictions based off model 2, because it makes fewer type II errors (false negatives). It is more cost effective for the lending company to ensure that high risk loans are classifed correctly as they may cause the company to lose profit if borrowers are unable to pay back the loans. Additionally, the over sampled regression model produced a higher recall and balanced accuracy score which may indicate the the prediction model makes fewer mistakes when classifying high risk loans. 

