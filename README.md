# Breast cancer classification and Streamlit deployment
- **BITS ID:** 2026AJ05136
- **Name:** Bachcha Ram Harijan

## 1. Problem Statement:
The objective of this project is to compare different five binary classification model to identify whether the breast cancer if Malignant or Benign and deploy the coparision of all five model in interactive web app using streamlit. This will show the metrics comparision and overall efficiency of the models.

## 2. Dataset description:
Dataset: Wisconsin Diagnostic Breast Cancer Dataset

Source: UCI Machine Learning Repository, accessed through scikit-learn.

Number of instances: 569

Number of input features: 30

Target classes:

0: Malignant
1: Benign   

The features are numerical measurements computed from digitized images of breast-mass fine-needle aspirates. They describe characteristics such as radius, texture, perimeter, area, smoothness and compactness.

## 3. Github repository link:
https://github.com/2026aj05brh/ML-Assignment2\

## 4. Live streaming application link:

## 5. Model used:
1. Logistic regression
2. Decision tree classifier
3. K-Neighbour classifier
4. Gaussian Naive Bayes
5. Support vector machine

## 6. Model metric comparison:
|ML model name | Accuracy | AUC | Precision | Recall | F1 | MCC|   
|-----------------|-------|-----|---------|--------|-----|-----|
| Logistic regression | 0.98  |  0. | 0 | 0| 
| Decision tree              |  0.99 | 0. | 
| KNN                        |  0.88    0. |  
| Naive Bayes                |  0.45    0.| 
| Support vector machine      | 0.12    0.| 

The above values were calculated on the same holdout test set data using random_state=42

## 7. Model observations
| Model name | Observations|
|------------|-------------|
| Logistic regression ||
| Decision tree              |  |
| KNN                        | |
| Naive Bayes                |  |
| Support vector machine |  |

## Overall winner model
The winner model is 
It was selected as a overall winner model because it obtained ---.MCC was used as the primary comparison evaluation metric because it considers
all four entries of the confusion matrix.

## Streamlit Application Features:
- CSV test-data uploaded
- Dropdowm menu for selecting a trained model out of all five model
- Accuracy, AUC, Recall, Precision, F1 Score and MCC for the selected model
- Confusion matrix
- Classification report
- Prediction-result download
- Evaluation without model training

## repository Structure:
'
├── app.py
├── train_models.py
├── requirements.txt
├── README.md
├── test_data.csv
├── results.csv
└──model/
   ├── decision_tree.joblib
   ├── feature_names.joblib
   ├── knn.joblib
   ├── logistic_regression.joblib
   ├── naive_bayes.joblib
   ├── support_vector_machine.joblib

