REPORT ON ARTIFICIAL NEURAL NETWORK CLASSIFICATION AND REGRESSION
CLASSIFICATION ANALYSIS: 
Overview of the dataset:
I have taken a Loan Dataset for Classification analysis using Artificial Neural Network.
The dataset contains transaction self-employed, applicant income, co-applicant income, loan amount, credit history and property area as independent variables/inputs/source and dependent variable/output/target are loan status.

Preprocessing of the dataset:
I did preprocessing using KNN Imputer where some columns had missing values. Converted categorical data to numerical using Label Encoder for self-employed and One Hot Encoder for property area.
Splitting the dataset into the Training set and Test set 20% and 80% respectively. Scaling the data using Standard Scalar.

ANN process:
Initialised ANN using ann = tf.keras.models.Sequential()
Created and added input layer and first layer with 6 units
Created and added second input layer with 6 units
Created and added the output layer with 1 unit because we have only one variable with 2 types of values 0 or 1

 Compiling using code
ann.compile(optimizer = 'adam', loss = 'binary_crossentropy', metrics =
['accuracy'])
Training the ann model with batch size 30 and epochs 100 times
ann.fit(X_train, y_train, batch_size = 30, epochs = 100)
Observation:
Making the predictions and evaluating the Model
Predicting the result for single observation
Use our ANN model to predict if the customer with the following information will receive a loan offer or not:
Self_Employed: No
Applicant Income: 3400$
Co Applicant Income: 1000$ LoanAmount: 500$
Credit_History: Yes
Property_Area: Urban
So, can we say no loan to that customer ?
First 3 column represents Property_Area, then Self_Employment, ApplicantIncome, CoapplicantIncome, Loan_Amount, Credit_History
Vamsi Krishna 008458886
 
 ANN model is predicting customer will get a loan with above details
Predicting the result for second observation
Use our ANN model to predict if the customer with the following information will receive a loan offer or not:
Self_Employed: No Applicant Income: 5000$ Co Applicant Income: 2000$ LoanAmount: 1000$ Credit_History: No Property_Area: SemiUrban
So, can we say no loan to that customer ?
First 3 column represents Property_Area, then Self_Employment, ApplicantIncome, CoapplicantIncome, Loan_Amount, Credit_History
Vamsi Krishna 008458886
print(ann.predict(sc.transform([[ 0.0, 0.0, 1.0, 0.0, 3400, 1000, 500,
1.0]])) > 0.5)
1/1 [==============================] - 0s 85ms/step
[[ True]]
 print(ann.predict(sc.transform([[ 0.0, 1.0, 0.0, 1.0, 5000, 2000, 1000,
0.0]])) > 0.5)
1/1 [==============================] - 0s 118ms/step
[[False]]
 

ANN model is predicting the customer will not get a loan with above details.
REGRESSION ANALYSIS: Overview of the dataset:
I have taken a Real Estate Dataset for regression analysis using Artificial Neural Network
The dataset contains transaction date, house age, distance to the nearest MRT station, number of convenience stores, latitude and longitude as independent variables/inputs/source and dependent variable/output/target is house price of unit area.
I used R-Squared, Mean-Squared Error, Root-Mean-Squared Error, Normalized Root-Mean-Squared Value and Mean Absolute Error Values to know how to model ANN for the above data set.
Preprocessing of the dataset:
Splitting the dataset into the Training set and Test set 20% and 80% respectively. Scaling the data using Standard Scalar.
ANN process:
Initialised ANN using ann = tf.keras.models.Sequential()
Created and added input layer and first layer with 6 units
Created and added second input layer with 6 units
Created and added the output layer with 1 unit because we have only one variable with 2 types of values 0 or 1
Compiling using code
ann.compile(optimizer = 'adam', loss = 'mean_squared_error')
 
 Training the ann model with batch size 32 and epochs 100 times
ann.fit(X_train, y_train, batch_size = 32, epochs = 100) Observation:
R-Squared Value:
The R-squared value, a measure of the goodness of fit, is 0.7023.
 This indicates that approximately 70.23% of the variability in the dependent variable is explained by the model.
Mean Squared Error (MSE):
The Mean Squared Error is 51.7102.
MSE measures the average squared difference between predicted and actual Values.
Lower MSE values indicate better model performance.
Root Mean Squared Error (RMSE):
The Root Mean Squared Error is 7.191.
RMSE is the square root of the MSE and provides a more interpretable measure in the same units as the target variable.
Lower RMSE values indicate better predictive accuracy.
Normalized Root Mean Squared Error (NRMSE):
The Normalized Root Mean Squared Error is 10.9954.
NRMSE is the RMSE normalized by the range of the target variable. It provides a relative measure of model accuracy.

 Mean Absolute Error (MAE):
The Mean Absolute Error is 14.0689.
MAE measures the average absolute difference between predicted and actual values.
Lower MAE values indicate better model accuracy without the influence of squared differences.
Summary Interpretation:
The R-squared value suggests that the model explains a significant portion of the variability in the target variable.
The MSE, RMSE, NRMSE, and MAE values collectively indicate the accuracy and performance of the Artificial Neural Network.

