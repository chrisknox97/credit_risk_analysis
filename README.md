# Supervised Machine Learning & Credit Risk

## Overview of the Analysis

### To utilize oversampling algorithims (RandomOverSampler, SMOTE), undersampling algorithms (ClusterCentroids), combinational algorithms (SMOTEENN), and machine learning models (BalancedRandomForestClassifier, EasyEnsembleClassifier); determining which presents the best predictive measures of credit risk. 

## Results

### As referneced above there were six algorithms used to predict credit risk, using a credit card dataset from LendingClub. The results of these algorithms are listed below:

### Balanced Accuracy Scores

| RandomOverSampler | SMOTE            | ClusterCentroids | SMOTEENN | BalancedRandomForestClassifier | EasyEnsembleClassifier |
| ----------------- | ---------------- | ---------------- | -------- | ------------------------------ | ---------------------- |
| 64%               | 65%              | 54%              | 64%      | 79%                            |  **93%**               |

### Precision Scores

|               | RandomOverSampler | SMOTE            | ClusterCentroids | SMOTEENN | BalancedRandomForestClassifier | EasyEnsembleClassifier |
| ------------- | ----------------- | ---------------- | ---------------- | -------- | ------------------------------ | ---------------------- |
| High Risk     | 0.01              | 0.01             | 0.01             | 0.01     | 0.03                           | **0.09**               |
| Low Risk      | **1.00**          | **1.00**         | 0.99             | 0.99     | **1.00**                       | **1.00**               |
| Overall Risk  | **0.99**          | **0.99**         | **0.99**         | **0.99** | **0.99**                       | **0.99**               |

### Recall Scores

|               | RandomOverSampler | SMOTE            | ClusterCentroids | SMOTEENN | BalancedRandomForestClassifier | EasyEnsembleClassifier |
| ------------- | ----------------- | ---------------- | ---------------- | -------- | ------------------------------ | ---------------------- |
| High Risk     | 0.66              | 0.61             | 0.69             | 0.72     | 0.70                           | 0.92                   |
| Low Risk      | 0.62              | 0.69             | 0.40             | 0.57     | 0.87                           | 0.94                   |
| Overall Risk  | 0.62              | 0.69             | 0.40             | 0.57     | 0.87                           | 0.94                   |

### F-1 Scores


|               | RandomOverSampler | SMOTE            | ClusterCentroids | SMOTEENN | BalancedRandomForestClassifier | EasyEnsembleClassifier |
| ------------- | ----------------- | ---------------- | ---------------- | -------- | ------------------------------ | ---------------------- |
| High Risk     | 0.02              | 0.02             | 0.01             | 0.02     | 0.06                           | 0.16                   |
| Low Risk      | 0.76              | 0.81             | 0.57             | 0.72     | 0.93                           | 0.97                   |
| Overall Risk  | 0.76              | 0.81             | 0.56             | 0.72     | 0.93                           | 0.97                   |

## Summary
