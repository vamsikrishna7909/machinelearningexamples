REPORT ON MACHINE LEARNING CLASSIFICATION MODELS
Overview of the dataset:
I have taken a Loan Dataset to analyze and evaluate which classification model is best suited for prediction out of Logistic Regression, K-Nearest Neighbor Regression, Support Vector, Decision Tree, and Random Forest Classifications.
The dataset contains transaction self-employed, applicant income, co-applicant income, loan amount, credit history and property area as independent variables/inputs/source and dependent variable/output/target are loan status.
I used Confusion Matrix, Accuracy, Precision, Recall and F1 scores to evaluate the best fit model for the above data set.
Logistic Regression:
Confused matrix = [[14 19] [ 2 88]]
Accuracy score = 0.8292682926829268 Precision score = 0.822429906542056
Recall score = 0.9777777777777777
F1 score = 0.8934010152284264
Observation-
The Logistic Regression classifier demonstrates a high accuracy score and strong precision, recall, and F1 score. It excels in correctly classifying both classes, as indicated by high precision and recall values. This model is well-balanced in terms of classifying the two classes.
K-Nearest Neighbor Classification:
Observation-
The K-Nearest Neighbors classifier also performs well with an accuracy of 0.805, along with commendable precision, recall, and F1 score. It correctly classifies both classes, demonstrating a good balance between precision and recall.
Support Vector Classification:
Vamsi Krishna 008458886
 Confused matrix = [[17 16] [ 8 82]]
Accuracy score = 0.8048780487804879 Precision score = 0.8367346938775511 Recall score = 0.9111111111111111
F1 score = 0.8723404255319148
 Confused matrix = [[14 19]
 [ 2 88]]
 Accuracy score = 0.8292682926829268
  Precision score = 0.822429906542056
  Recall score = 0.9777777777777777
  F1 score = 0.8934010152284264
 Observation-
Support Vector Classifier (SVC) exhibits similar performance to Logistic Regression with high accuracy and strong precision, recall, and F1 score. It effectively classifies both classes.

Decision Tree Classification:
Observation-
The Decision Tree classifier has a lower accuracy score compared to the previous models. While it has a reasonable precision score, it struggles with recall, indicating that it does not capture all instances of the first class effectively. This suggests a potential issue with overfitting.
Random Forest Classification:
Vamsi Krishna 008458886
 Confused matrix = [[20 13] [25 65]]
Accuracy score = 0.6910569105691057 Precision score = 0.8333333333333334 Recall score = 0.7222222222222222
F1 score = 0.7738095238095238
 Confused matrix = [[20 13] [12 78]]
Accuracy score = 0.7967479674796748 Precision score = 0.8571428571428571 Recall score = 0.8666666666666667
F1 score = 0.861878453038674
Observation-
The Random Forest classifier offers improved performance over the Decision Tree with a slightly higher accuracy score. It maintains strong precision and recall values, resulting in a balanced F1 score.

Summary:
Logistic Regression, K-Nearest Neighbors, and the Support Vector Classifier appear to be the best models for this dataset. They have high accuracy and strong precision and recall scores, indicating effective classification of both classes. The Decision Tree, while not performing as well, still shows reasonable precision but falls short in recall, potentially due to overfitting. The Random Forest improves upon the Decision Tree and provides a balanced classification performance.