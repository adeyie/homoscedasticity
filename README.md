# Homoscedasticity Assumption in Linear Regression
Linear regression is one of the most commonly used techniques for modeling the relationship between input variables and a continuous target variable. However, linear regression relies on several key assumptions, one of which is homoscedasticity.

In this write-up, I will discuss:
* What the homoscedasticity assumption is?
* How to identify whether a dataset meets the homoscedasticity assumption?
* What to do if a dataset violates the homoscedasticity assumption?
## Homoscedasticity
The regression models are trained by minimizing least squares errors between fitted values and true values from a training dataset. This model of regression is known as the ordinary least squares (OLS) regression. The coefficient of input variables and the intercept are estimated by minimizing the least squares errors. From the known values of coefficients and intercepts, the point value of the target variable is estimated for a new observation. The OLS regression assumes that the error is consistent for all observations, known as homoscedasticity. 
