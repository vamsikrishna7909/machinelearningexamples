Loan Prediction Analysis using Machine Learning Classification Models

Overview
This project analyzes and evaluates various classification models to predict loan status. The dataset includes features such as:

Transaction type (e.g., self-employed)
Applicant income
Co-applicant income
Loan amount
Credit history
Property area
The target variable is loan status.

Classification Models Evaluated:
The following models were tested to identify the best fit for the dataset:

Logistic Regression
K-Nearest Neighbor (KNN)
Support Vector Classification (SVC)
Decision Tree
Random Forest
Evaluation Metrics:
To determine the performance of each model, I used the following metrics:

Confusion Matrix
Accuracy
Precision
Recall
F1 Score
Results:
1. Logistic Regression

Confusion Matrix: [[14 19], [2 88]]
Accuracy: 82.9%
Precision: 82.24%
Recall: 97.77%
F1 Score: 89.34%
Observation: The Logistic Regression model demonstrates high accuracy, precision, recall, and F1 score. It effectively balances classifying both categories.

2. K-Nearest Neighbor (KNN)

Accuracy: 80.5%
Precision, Recall, F1 Score: Comparable to Logistic Regression.
Observation: KNN performs well with commendable accuracy, precision, recall, and F1 score, indicating good classification balance.

3. Support Vector Classification (SVC)

Confusion Matrix: [[17 16], [8 82]]
Accuracy: 80.4%
Precision: 83.67%
Recall: 91.11%
F1 Score: 87.23%
Observation: SVC has similar performance to Logistic Regression, with strong precision, recall, and overall balanced classification.

4. Decision Tree

Observation: The Decision Tree classifier has a lower accuracy and struggles with recall, suggesting it may overfit to the data.
5. Random Forest

Confusion Matrix: [[20 13], [12 78]]
Accuracy: 79.6%
Precision: 85.71%
Recall: 86.66%
F1 Score: 86.18%
Observation: Random Forest shows improved performance over the Decision Tree, with a balanced F1 score and reliable precision and recall.

Summary:
Logistic Regression, KNN, and SVC are the top-performing models for this dataset, all demonstrating strong accuracy, precision, and recall. While the Decision Tree model underperforms due to potential overfitting, the Random Forest model improves upon this and offers a well-balanced performance.
