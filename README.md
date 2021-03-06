# Supervised Machine Learning & Credit Risk

## Overview of the Analysis

### To utilize oversampling algorithims (``RandomOverSampler``, ``SMOTE``), undersampling algorithms (``ClusterCentroids``), combinational algorithms (``SMOTEENN``), and machine learning models (``BalancedRandomForestClassifier``, ``EasyEnsembleClassifier``); determining which presents the best predictive measures of credit risk. 

## Results

### As referenced above, there were six algorithms used to predict credit risk, using a credit card dataset from LendingClub. The results of these algorithms are listed below with the highest measures in **bold**:

### Balanced Accuracy Scores

* A Balanced Accuracy Score is used with imbalanced datasets and attempts to account for that imbalance by combining sensitivity and specificity together, and dividing that measure in half. 
* Balanced Accuracy Scores are measured on a scale of 0-1; the closer the number is to 1, the more predictive said algorithm remains. 
* Of the Balanced Accuracy Scores in this dataset, ``EasyEnsembleClassifer`` easily topped all others, while ``ClusterCentroids`` came in dead last. 


| RandomOverSampler | SMOTE            | ClusterCentroids | SMOTEENN | BalancedRandomForestClassifier | EasyEnsembleClassifier |
| ----------------- | ---------------- | ---------------- | -------- | ------------------------------ | ---------------------- |
| 64%               | 65%              | 54%              | 64%      | 79%                            |  **93%**               |


### Precision Scores

* A Precision Score is a score that quantifies an algorithms ability to avoid false positives. 
* Similar to a Balanced Accuracy Score, precision is measured on a scale of 0-1, with the best measures remaining closer to 1. 
* Within this dataset, ``EasyEnsembleClassifer`` scored highest across all metrics, while ``ClusterCentroids`` and ``SMOTEENN`` scored the lowest. 

|               | RandomOverSampler | SMOTE            | ClusterCentroids | SMOTEENN | BalancedRandomForestClassifier | EasyEnsembleClassifier |
| ------------- | ----------------- | ---------------- | ---------------- | -------- | ------------------------------ | ---------------------- |
| High Risk     | 0.01              | 0.01             | 0.01             | 0.01     | 0.03                           | **0.09**               |
| Low Risk      | **1.00**          | **1.00**         | 0.99             | 0.99     | **1.00**                       | **1.00**               |
| Overall Risk  | **0.99**          | **0.99**         | **0.99**         | **0.99** | **0.99**                       | **0.99**               |

### Recall Scores

* A Recall Score is a score used to quantify the amount of 'true' positives against actual positive results. 
* Like our previous measures, recall is measured on a scale of 0-1, with scores closer to 1 remaining preferable. 
* Our dataset's highest recall scores across all metrics belonged to ``EasyEnsembleClassifer`` while the lowest belonged to ``ClusterCentroids``.

|               | RandomOverSampler | SMOTE            | ClusterCentroids | SMOTEENN | BalancedRandomForestClassifier | EasyEnsembleClassifier |
| ------------- | ----------------- | ---------------- | ---------------- | -------- | ------------------------------ | ---------------------- |
| High Risk     | 0.66              | 0.61             | 0.69             | 0.72     | 0.70                           | **0.92**               |
| Low Risk      | 0.62              | 0.69             | 0.40             | 0.57     | 0.87                           | **0.94**               |
| Overall Risk  | 0.62              | 0.69             | 0.40             | 0.57     | 0.87                           | **0.94**               |

### F-1 Scores

* Finally, the F-1 Score is the mean of our precision and recall scores; as such it can be useful if either recall or precision remains particuarly skewed. 
* As such, F-1 Scores are measured on a 0-1 scale, with scores nearest to 1 representing the most predictive algorithms. 
* For our dataset, ``EasyEnsembleClassifer`` had the best results across all metrics, while ``ClusterCentroids`` once again had the worst. 


|               | RandomOverSampler | SMOTE            | ClusterCentroids | SMOTEENN | BalancedRandomForestClassifier | EasyEnsembleClassifier |
| ------------- | ----------------- | ---------------- | ---------------- | -------- | ------------------------------ | ---------------------- |
| High Risk     | 0.02              | 0.02             | 0.01             | 0.02     | 0.06                           | **0.16**               |
| Low Risk      | 0.76              | 0.81             | 0.57             | 0.72     | 0.93                           | **0.97**               |
| Overall Risk  | 0.76              | 0.81             | 0.56             | 0.72     | 0.93                           | **0.97**               |

### Screenshots

* Screenshots of these Balanced Accuracy Scores can be found [here](https://github.com/chrisknox97/credit_risk_analysis/tree/main/PNGs/Balanced%20Accuracy).
* Screenshots of these Classification Reports can be found [here](https://github.com/chrisknox97/credit_risk_analysis/tree/main/PNGs/Classification%20Report).

## Summary

### The results of this dataset remained rather clear cut across all metrics (Balanced Accuracy, Precision, Recall, & F-1 Scores), with ``EasyEnsembleClassifer`` notching the highest measures. Similarly, ``ClusterCentroids`` reatined the lowest measures across all our metrics, while ``BalancedRandomForestClassifier`` represented a viable alternative with its metrics trailing only the aforementioned ``EasyEnsembleClassifer``. 

### As such, out of the six algorithms tested against the LendingClub dataset, we suggest using ``EasyEnsembleClassifer`` due to its high accuracy, precision and recall. Additionally, we would also suggest ``BalancedRandomForestClassifier`` as a viable alternative, albeit less enthusiastically. 

