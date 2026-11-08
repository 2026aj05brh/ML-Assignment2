# Breast cancer classification and Streamlit deployment
**Assignment2: Machine Learning**   
**BITS ID:** 2026AJ05136   
**Name:** Bachcha Ram Harijan

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
| Logistic regression |0.9825|0.9954|0.9861|0.9861|0.9861|0.9623
| Decision tree       |0.9211|0.9163|0.9565|0.9167|0.9362|0.8341|
| KNN                 |0.9561|0.9788|0.9589|0.9722|0.9655|0.9054|
| Naive Bayes         |0.9386|0.9878|0.9452|0.9583|0.9517|0.8676|
| Support vector machine|0.9825|0.9950|0.9861|0.9861|0.9861|0.9623|

The above values were calculated on the same holdout test set data using random_state=42

## 7. Model observations
| Model name | Observations|
|------------|-------------|
| Logistic regression |Logistic Regression achieved an accuracy of 98.25%, an AUC of 99.54%, and an MCC of 96.23%. It provided an excellent balance between precision and recall, with both reaching 98.61%. The high AUC indicates that the model can distinguish effectively between Malignant and Benign observations. Logistic Regression was selected as the best model because it achieved the highest AUC while tying for the highest Accuracy, F1-score, and MCC.|
| Decision tree |Decision Tree achieved an accuracy of 92.11% and an MCC of 83.41%, which were the lowest values among the evaluated models. Its precision of 95.65% was relatively strong, but its lower recall of 91.67% indicates that it missed more positive observations. The model is easy to interpret, but a single tree was less capable of generalizing to the test data than Logistic Regression, KNN, Naive Bayes, and SVM.|
| KNN             |K-Nearest Neighbors achieved an accuracy of 95.61%, an AUC of 97.88%, and an MCC of 90.54%. Its recall of 97.22% was higher than its precision of 95.89%, indicating that the model detected most positive cases but generated slightly more false-positive predictions. Standardization was necessary because KNN calculates distances between observations. Overall, KNN performed well but did not match Logistic Regression or SVM. |
| Naive Bayes                | Gaussian Naive Bayes achieved an accuracy of 93.86%, an AUC of 98.78%, and an MCC of 86.76%. The high AUC indicates strong class-ranking ability, but its lower Accuracy and MCC show that the final class predictions were less balanced than those of Logistic Regression and SVM. |
| Support vector machine | Support Vector Machine achieved an accuracy of 98.25%, an AUC of 99.50%, and an MCC of 96.23%. It tied with Logistic Regression on Accuracy, Precision, Recall, F1-score, and MCC. This indicates that both models produced almost identical classification quality. However, the SVM had a slightly lower AUC and is more difficult to interpret than Logistic Regression. |
| Overall, Winner for my dataset|Logistic Regression. Because among the five evaluated classifiers, Logistic Regression and Support Vector Machine produced the strongest results. Both achieved 98.25% Accuracy, 98.61% Precision, 98.61% Recall, a 98.61% F1-score, and an MCC of 96.23%. Logistic Regression was selected as the final best model because it achieved the highest AUC of 99.54%, compared with 99.50% for SVM. Logistic Regression is also simpler and more interpretable than the RBF Support Vector Machine. KNN ranked third with an MCC of 90.54%, while Naive Bayes showed strong ranking ability with an AUC of 98.78% but lower threshold-based performance. Decision Tree produced the weakest overall results, with the lowest Accuracy, AUC, F1-score, and MCC.|

## 8. Overall winner model
The winner model is Logistic Regression
It was selected as a overall winner model because among the all five evaluated classifiers, Logistic Regression and Support Vector Machine produced the strongest results. Both achieved 98.25% Accuracy, 98.61% Precision, 98.61% Recall, a 98.61% F1-score, and an MCC of 96.23%. Logistic Regression was selected as the final best model because it achieved the highest AUC of 99.54%, compared with 99.50% for SVM.

## 9. Streamlit Application Features:
- CSV test-data uploaded
- Dropdowm menu for selecting a trained model out of all five model
- Accuracy, AUC, Recall, Precision, F1 Score and MCC for the selected model
- Confusion matrix
- Classification report
- Prediction-result download
- Evaluation without model training

## 10. GitHub Repository Structure:
````text
.
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



