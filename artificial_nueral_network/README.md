# Artificial Neural Network (ANN) Classification and Regression

## Classification Analysis

### Overview of the Dataset
This project analyzes a Loan Dataset for classification using Artificial Neural Networks (ANN). The dataset includes the following features as independent variables:
- Self-employed status
- Applicant income
- Co-applicant income
- Loan amount
- Credit history
- Property area

The target variable is the loan status.

### Preprocessing of the Dataset
- Handled missing values using **KNN Imputer**.
- Converted categorical data:
  - Used **Label Encoder** for `self-employed`.
  - Applied **One Hot Encoder** for `property area`.
- Split the dataset into **80% training** and **20% test** sets.
- Scaled the data using **Standard Scaler**.

### ANN Model Process
- **Initialized the ANN** using:  
  `ann = tf.keras.models.Sequential()`
- Created and added:
  - First input layer with 6 units.
  - Second hidden layer with 6 units.
  - Output layer with 1 unit (binary classification: 0 or 1).
- **Compiled the model** using:  
  `ann.compile(optimizer = 'adam', loss = 'binary_crossentropy', metrics = ['accuracy'])`
- Trained the model with:
  - **Batch size**: 30
  - **Epochs**: 100  
  `ann.fit(X_train, y_train, batch_size = 30, epochs = 100)`

### Predictions and Model Evaluation
#### Example 1:
**Input:**
- Self-employed: No
- Applicant Income: $3400
- Co-applicant Income: $1000
- Loan Amount: $500
- Credit History: Yes
- Property Area: Urban

**Prediction:**  
The ANN model predicts that the customer will **receive a loan**.

#### Example 2:
**Input:**
- Self-employed: No
- Applicant Income: $5000
- Co-applicant Income: $2000
- Loan Amount: $1000
- Credit History: No
- Property Area: SemiUrban

**Prediction:**  
The ANN model predicts that the customer will **not receive a loan**.

---

## Regression Analysis

### Overview of the Dataset
For regression analysis, I used a Real Estate Dataset. The independent variables include:
- Transaction date
- House age
- Distance to the nearest MRT station
- Number of convenience stores
- Latitude
- Longitude

The target variable is the **house price of a unit area**.

### Preprocessing of the Dataset
- Split the dataset into **80% training** and **20% test** sets.
- Scaled the data using **Standard Scaler**.

### ANN Model Process
- **Initialized the ANN** using:  
  `ann = tf.keras.models.Sequential()`
- Created and added:
  - First input layer with 6 units.
  - Second hidden layer with 6 units.
  - Output layer with 1 unit (regression task).
- **Compiled the model** using:  
  `ann.compile(optimizer = 'adam', loss = 'mean_squared_error')`
- Trained the model with:
  - **Batch size**: 32
  - **Epochs**: 100  
  `ann.fit(X_train, y_train, batch_size = 32, epochs = 100)`

### Model Evaluation
- **R-Squared Value:** 0.7023  
  This indicates that approximately 70.23% of the variability in the house price is explained by the model.
- **Mean Squared Error (MSE):** 51.7102  
  MSE measures the average squared difference between predicted and actual values. Lower MSE indicates better performance.
- **Root Mean Squared Error (RMSE):** 7.191  
  RMSE is the square root of MSE and provides a more interpretable metric in the same units as the target variable.
- **Normalized Root Mean Squared Error (NRMSE):** 10.9954  
  NRMSE is RMSE normalized by the range of the target variable.
- **Mean Absolute Error (MAE):** 14.0689  
  MAE measures the average absolute difference between predicted and actual values. Lower MAE values indicate better accuracy.

### Summary Interpretation
- The **R-Squared** value suggests that the model explains a significant portion of the target variable's variability.
- The combination of **MSE**, **RMSE**, **NRMSE**, and **MAE** provides a comprehensive view of the ANN's predictive accuracy and performance for this regression task.
