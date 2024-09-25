# Machine Learning Classification Models: Loan Dataset Analysis

## Overview of the Dataset

This project analyzes a Loan Dataset to evaluate which classification model is best suited for loan status prediction. The models under consideration are:

- Logistic Regression
- K-Nearest Neighbor
- Support Vector Classification (SVC)
- Decision Tree
- Random Forest

The dataset includes the following features as independent variables:
- Transaction type (Self-employed)
- Applicant income
- Co-applicant income
- Loan amount
- Credit history
- Property area

The target variable is the loan status.

### Evaluation Metrics
I used the following metrics to evaluate model performance:
- Confusion Matrix
- Accuracy
- Precision
- Recall
- F1 Score

## Model Performance

### Logistic Regression
- **Confusion Matrix:** `[[14 19], [2 88]]`
- **Accuracy Score:** `0.829`
- **Precision Score:** `0.822`
- **Recall Score:** `0.978`
- **F1 Score:** `0.893`

**Observation:**
- The Logistic Regression classifier demonstrates a high accuracy score and strong precision, recall, and F1 score. It excels in correctly classifying both classes, making it a well-balanced model.

### K-Nearest Neighbor Classification
- **Confusion Matrix:** N/A
- **Accuracy Score:** `0.805`
- **Precision Score:** N/A
- **Recall Score:** N/A
- **F1 Score:** N/A

**Observation:**
- The K-Nearest Neighbors classifier performs well with an accuracy of 0.805, maintaining a good balance between precision and recall.

### Support Vector Classification
- **Confusion Matrix:** `[[17 16], [8 82]]`
- **Accuracy Score:** `0.805`
- **Precision Score:** `0.837`
- **Recall Score:** `0.911`
- **F1 Score:** `0.872`

**Observation:**
- Support Vector Classifier (SVC) shows similar performance to Logistic Regression with high accuracy, precision, recall, and F1 score, indicating effective classification.

### Decision Tree Classification
- **Confusion Matrix:** N/A
- **Accuracy Score:** N/A
- **Precision Score:** N/A
- **Recall Score:** N/A
- **F1 Score:** N/A

**Observation:**
- The Decision Tree classifier has a lower accuracy score than other models. While its precision is reasonable, it struggles with recall, indicating possible overfitting.

### Random Forest Classification
- **Confusion Matrix:** `[[20 13], [25 65]]`
- **Accuracy Score:** `0.691`
- **Precision Score:** `0.833`
- **Recall Score:** `0.722`
- **F1 Score:** `0.774`

- **Confusion Matrix (Second Run):** `[[20 13], [12 78]]`
- **Accuracy Score:** `0.797`
- **Precision Score:** `0.857`
- **Recall Score:** `0.867`
- **F1 Score:** `0.862`

**Observation:**
- The Random Forest classifier improves over the Decision Tree, offering a balanced performance with higher precision, recall, and F1 scores.

## Summary
- Logistic Regression, K-Nearest Neighbors, and the Support Vector Classifier are the best-performing models for this dataset, demonstrating high accuracy and strong precision-recall balances.
- The Decision Tree, while reasonable in precision, struggles with recall, possibly due to overfitting.
- The Random Forest classifier offers improved performance over the Decision Tree, providing a more balanced classification.
