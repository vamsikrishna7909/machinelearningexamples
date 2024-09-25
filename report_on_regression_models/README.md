REPORT ON MACHINE LEARNING REGRESSION MODELS

Overview of the dataset:
    I have taken a Real Estate Dataset to analyze and evaluate which regression model is best suited for prediction out of Multiple Linear Regression, Polynomial Regression, Support Vector Regression, Decision Tree Regression and Random Forest Regression.

The dataset contains transaction date, house age, distance to the nearest MRT station, number of convenience stores, latitude and longitude as independent variables/inputs/source and  dependent variable/output/target is house price of unit area.

I used R-Squared, Mean-Squared Error, Root-Mean-Squared Error, Normalized Root-Mean-Squared Value and Mean Absolute Error Values to evaluate the best fit model for the above data set.

Multiple Linear Regression:

The R-Squared value is: 0.6573242742218073
The Mean Squared Error value is: 59.522435319024204
The Root Mean Squared Error value is: 7.715078438941772
The Normalize Root Mean Squared Error value is: 11.796756022846749
The Mean Absolute Error value is: 16.96835291350557
Observation-
In Multiple Linear Regression, the R-squared value is above 0.5 i.e  0.6573242742218073 i.e 0.6573 indicates that approximately 65.73% of the variance in the target variable explained by the model and we can assume that model has a moderative predictive power with relatively low Mean Squared Error, indicating a reasonably good fit. The Root Mean Squared Error suggests an average prediction error.
Polynomial Regression :
The R-Squared value is: 0.6579977654760951
The Mean Squared Error value is: 59.40545055294472
The Root Mean Squared Error value is: 7.7074931432304705
The Normalize Root Mean Squared Error value is: 11.785157711361578
The Mean Absolute Error value is: 16.449913265554564
Observation-
The Polynomial Regression model performs similarly to Multiple Linear Regression. It has an R-squared value of 0.6579977654760951 i.e 6.6580, which indicates that about 65.80% of the variance is explained by the model. The Mean Squared Error is slightly lower, and the Root Mean Squared Error is similar. The model's performance is moderate, with a Mean Absolute Error of 16.45.
Support Vector Regression :
The R-Squared value is: 0.7044881583675278
The Mean Squared Error value is: 51.330115197479564
The Root Mean Squared Error value is: 7.164503834703389
The Normalize Root Mean Squared Error value is: 10.954898829821696
The Mean Absolute Error value is: 14.430131154033642
Observation-
Support Vector Regression (SVR) outperforms the previous models with an R-squared value of 0.7045, suggesting that it explains approximately 70.45% of the variance in the target variable. The Mean Squared Error and Root Mean Squared Error are relatively low, indicating better model performance. The Mean Absolute Error is 14.43, suggesting that the SVR model has a lower average prediction error.
Decision Tree Regression :
The R-Squared value is: 0.16425800123264644
The Mean Squared Error value is: 145.16756024096384
The Root Mean Squared Error value is: 12.048550130242386
The Normalize Root Mean Squared Error value is: 18.42285952636451
The Mean Absolute Error value is: 18.78562773664168
Observation-
The Decision Tree Regression model has a lower R-squared value (0.1643), indicating that it explains only 16.43% of the variance in the target variable. The Mean Squared Error is high, and the Root Mean Squared Error is relatively large, suggesting that the model does not fit the data well. The Mean Absolute Error is also high at 18.79, indicating a larger average prediction error.
 
Random Forest Regression :
The R-Squared value is: 0.6767353359686661
The Mean Squared Error value is: 56.150753053882205
The Root Mean Squared Error value is: 7.493380615842372
The Normalize Root Mean Squared Error value is: 11.457768525752863
The Mean Absolute Error value is: 13.431692575788038
Observation-
The Random Forest Regression model performs well with an R-squared value of 0.6767, explaining about 67.67% of the variance in the target variable. The model has a lower Mean Squared Error, Root Mean Squared Error, and Mean Absolute Error compared  to the Multiple Regression, Polynomial Regression, Decision Tree model. It provides a better fit to the data and lower prediction errors.
Summary:
    Support Vector Regression and Random Forest Regression models appear to be the better-performing models among the options I have considered for evaluation, with SVR having a slightly higher R-squared value and lower prediction errors. However, the choice of the best model may also depend on other factors like model complexity, interpretability, and computational requirements.But for the above data set SVR and Random Forest Regression Models are best fit.

