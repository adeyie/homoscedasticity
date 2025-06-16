# Homoscedasticity Assumption in Linear Regression
Linear regression is one of the most commonly used techniques for modeling the relationship between input variables and a continuous target variable. However, linear regression relies on several key assumptions, one of which is homoscedasticity.

In this write-up, I will discuss:
* What the homoscedasticity assumption is?
* How to identify whether a dataset meets the homoscedasticity assumption?
* What to do if a dataset violates the homoscedasticity assumption?
## Homoscedasticity
The regression models are trained by minimizing least squares errors between fitted values and true values from a training dataset. This model of regression is known as the ordinary least squares (OLS) regression. The coefficient of input variables and the intercept are estimated by minimizing the least squares errors. From the known values of coefficients and intercepts, the point value of the target variable is estimated for a new observation. The OLS regression assumes that the error is consistent for all observations, known as homoscedasticity. 

For example, the following figure shows residuals vs. fitted values from a dataset that meets the homoscedasticity assumption.

![image alt](https://github.com/adeyie/homoscedasticity/blob/50cebaafa85242bf6f60e32f5bd85b153b3ae5c3/homoscedasticity.png)

The figure below shows a dataset that violates the homoscedasticity assumption. This condition is known as heteroscedasticity.

![image alt](https://github.com/adeyie/homoscedasticity/blob/9d4d0c974b65510b6fadee4994b89952a2be59b8/heteroscedasticity.png)

##  Checking the Homoscedasticity Assumption
To evaluate whether a dataset meets the homoscedasticity assumption in linear regression, develop an Ordinary Least Squares (OLS) regression model by minimizing least squares errors. Formula for model parameter estimation,
<pre> β = (XᵀX)⁻¹Xᵀy </pre>
Next, calculate the fitted (predicted) values and residuals for each data point. Then, create a plot with the fitted values on the x-axis and the residuals on the y-axis. 
<pre> residual=actual value-fitted value</pre>
If the points are randomly scattered without any clear pattern, it suggests that the homoscedasticity assumption is likely satisfied. The parameters of the linear regression model are estimated by minimizing the sum of squared residuals, a method known as Ordinary Least Squares (OLS).

If the plot shows any visible pattern and is not randomly scattered, it suggests a violation of the homoscedasticity assumption. In such cases, you can use Weighted Least Squares (WLS) regression to estimate the model parameters.
## Weighted Least Squares (WLS) Regression
The model parameter estimation formulation for WLS regression is
<pre> β = (XᵀWX)⁻¹XᵀWy </pre>
