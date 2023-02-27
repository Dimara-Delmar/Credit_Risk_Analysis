# Credit Risk Analysis

## Overview

### Purpose 
Credit risk is an inherently imbalanced problem, as the number of low-risk loans usually outnumber the high-risk ones. Using the credit card dataset provided by LendingClub, we will be applying six different machine learning methods to compare each model’s accuracy, precision, and recall scores in relation to the data’s credit risk. The following analysis will be completed through these tasks: 

1)	Oversampling the data using the RandomOverSampler and SMORE algorithms.
2)	Undersampling the data using the ClusterCentroids algorithm.
3)	Using combination (over and under) sampling through the SMOTEEN algorithm.
4)	Comparing two machine learning models that are designed to reduce bias: BalancedRandomForestClassifier and EasyEnsembleClassifier.

## Resources
-	Data source: `LoanStats_2019Q1.csv`
-	Software used: Python, Jupiter Notebook, imbalanced-learn and scikit-learn libraries. 

## Results

### Naive Random Oversampling 

<img width="284" alt="NRO_accuracy" src="https://user-images.githubusercontent.com/108738297/221450811-7fe64ee1-8143-48e7-8b05-a153aed23564.PNG">

-	Balanced Accuracy Score: 65.73%

<img width="398" alt="NRO_class" src="https://user-images.githubusercontent.com/108738297/221450823-068cdc9e-8599-4fa0-9f59-1a1c2b5a68d3.PNG">

High Risk
  - Precision: 1%
  - Recall: 71%

Low Risk
  - Precision: 100%
  -	Recall: 60%

### SMOTE Oversampling

<img width="231" alt="SMOTE_accuracy" src="https://user-images.githubusercontent.com/108738297/221450850-33c8ebb8-d474-40d2-8714-81cf41ec0899.PNG">

-	Balanced Accuracy Score: 66.22%

<img width="394" alt="SMOTE_class" src="https://user-images.githubusercontent.com/108738297/221450865-bd2efabb-5a7a-4ba9-b6ee-2d2e911b4903.PNG">

High Risk
- Precision: 1%
- Recall: 63%

Low Risk
- Precision: 100%
- Recall: 69%

### Undersampling 

<img width="230" alt="Under_accuracy" src="https://user-images.githubusercontent.com/108738297/221450886-c0d243b7-a7a5-4347-ba4d-229036661eb9.PNG">

-	Balanced Accuracy Score: 54.47%

<img width="400" alt="Under_class" src="https://user-images.githubusercontent.com/108738297/221450899-98b5de03-d038-4446-a119-342b95929b39.PNG">

High Risk
- Precision: 1%
- Recall: 69%

Low Risk
- Precision: 100%
- Recall: 40%

### Combination (Over and Under)

<img width="228" alt="combo_accuracy" src="https://user-images.githubusercontent.com/108738297/221450917-16da15d0-eb0c-431a-b4aa-211fa1e548d6.PNG">

-	Balanced Accuracy Score: 64.47%

<img width="398" alt="combo_class" src="https://user-images.githubusercontent.com/108738297/221450929-1090d0c9-b834-4192-9664-1f379c61779c.PNG">

High Risk
- Precision: 1%
- Recall: 72%

Low Risk
- Precision: 100%
- Recall: 57%

### Balanced Random Forest Classifier

<img width="227" alt="BRFC_accuracy" src="https://user-images.githubusercontent.com/108738297/221450960-c269a0dc-91f3-450c-88cd-2d34ed2c2a96.PNG">

-	Balanced Accuracy Score: 78.85%

<img width="401" alt="BRFC_class" src="https://user-images.githubusercontent.com/108738297/221450954-7acd30a5-063d-49d6-8452-de2e5ea8411a.PNG">

High Risk
- Precision: 30%
- Recall: 70%

Low Risk
- Precision: 100%
- Recall: 87%

### Easy Ensemble AdaBoost Classifier 

<img width="235" alt="EEAC_accuracy" src="https://user-images.githubusercontent.com/108738297/221450997-2ed0c82e-c43f-4347-979b-7fce2d7d7e1c.PNG">

-	Balanced Accuracy Score: 93.16%

<img width="398" alt="EEAC_class" src="https://user-images.githubusercontent.com/108738297/221450987-5fb8d966-6e3c-4062-83d6-558c13b07ece.PNG">

High Risk
- Precision: 90%
- Recall: 92%

Low Risk
- Precision: 100%
- Recall: 94%

## Summary 
Out of all the machine learning models tested in this project, the Easy Ensemble AdaBoost Classifier performed the best in all categories of precision, accuracy, and recall. Most of the other models however (excluding the Balanced Random Forest Classifier), had repetitively low precision scores for all high-risk loan data, when compared to the precision scores of low-risk loan data. This disparity in performance makes the other models unreliable when it comes to both sensitivity and precision, which is essential in understanding credit risk. Due to this outcome, I’d recommended only using the Easy Ensemble AdaBoost Classifier for the best results. 

