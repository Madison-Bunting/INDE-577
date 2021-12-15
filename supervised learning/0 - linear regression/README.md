# Linear Regression

![image](https://cdn.analyticsvidhya.com/wp-content/uploads/2021/05/2.3.png)

Linear regression is a classic supervised model that dates back over 200 years. Finding a good rough linear fit to a set of points was performed by [Legendre](https://en.wikipedia.org/wiki/Adrien-Marie_Legendre) (1805) and [Gauss](https://en.wikipedia.org/wiki/Carl_Friedrich_Gauss) to predict planetary movement.

Linear regression has been around for over 200 years and has been studied from every possible. Often different angles have been given different names:
- linear model: a model that assumes a linear relationship between input variables (x) and a single output variable (y), with the goal of calculating y from a linear combination of the input variables (x)
- simple linear regression: when there is a single input variable (x)
- multiple linear regression: when there are multiple input variables

[Linear regression](https://en.wikipedia.org/wiki/Linear_regression) is a linear equation that combines a specific set of input values (x) to a predicted output (y). Both input and output variables are numeric. The linear equation assigns one scale factor to each input value (often denoted "m"), and a constant (often denoted "b") that gives the line an additional degree of freedom because it can move up and down on a 2D plot. Thus, we have the familiar equation from algebra: **y = mx + b**. In the image above, the red line is called the **line of best fit** that is described by the previous equation.

In higher dimensions, the line is called a plane or "hyperplane", and simply adds additional terms to the equation, as written below:

![image](https://user-images.githubusercontent.com/89811204/146124493-bc21822d-f66d-4a49-8767-cf8d449e4f18.png)

When the coefficient of one of these terms becomes zero, it effectively removes the influence of the input variable on the model.

Below are some sample techniques to prepare a linear regression model:
- **Simple linear regression:** The model has a single input and uses statistics to estimate coefficients. This requires computing statistical properties like means, standard deviations, correlations, and variance. 
- **Ordinary least squares** ("or ortinary least squares linear regression" or "least squares regression"): This is the most common technique. When there is more than one input, OSLR can estimate the values of the coefficients. The [Gauss-Markove theorem](https://en.wikipedia.org/wiki/Gauss%E2%80%93Markov_theorem) ensures this method minimizes the "sum of the squared residuals". This means that given a regression line through the data, calculate the distance from each datapoint to the regression point, square it, and sum all of the squared errors together. This approach treats the data as a matrix and uses linear algebra to estimate the optimal values for the coefficients. It requires memory to fit the data and perform matrix operations, but is very fast to calculate.
- **Gradient Descent:** This approach is further discussed [elsewhere](https://github.com/Madison-Bunting/INDE-577/blob/main/supervised%20learning/1%20-%20gradient%20descent/README.md) in this repository, but the short description is that this technique starts with random values for the coefficients, then iteratively works to minimize the error of the model.
- **Regularization:** These models seek to minimize the sum of the squared error of the model on training data using ordinary least squares, as well as reducing the complexity of the model. These methods are effective when input values have collinearity in input values and ordinary least squares would overfit the training data.
  - [Lasso Regression](https://en.wikipedia.org/wiki/Lasso_(statistics)) (aka L1 regularization): modifies ordinary least squares to also minimize the absolute sum of the coefficients
  - [Ridge Regression](https://en.wikipedia.org/wiki/Tikhonov_regularization) (aka L2 regularization): modifies ordinary least squares to mimize the squared absolute sum of the coefficients

There are a few assumptions underlying linear models:
- Linearity: the dependent variable Y should be linearly related to independent variables - this can be checked with a scatterplot

![image](https://editor.analyticsvidhya.com/uploads/96503linear-nonlinear-relationships.png)

- Normality: X and Y values follow the normal distrigution - this can be checked with histograms, KDE plots, or Q-Q plots

![image](https://editor.analyticsvidhya.com/uploads/64526normality.png)

- Homoscedasticity: The spread of the residuals should be constant for all variables - this can be checked with a residual plot (if the assumption is violated, points will form a funnel shape)

![image](https://editor.analyticsvidhya.com/uploads/51367residuals.png)

- Independence/No multicollinearity: there is no correlation between any of the independent variables - this can be checked with a correlation matrix of VIF score (if VIF > 5, variables are highly correlated)

![image](https://editor.analyticsvidhya.com/uploads/99214correlation.png)

- Error terms are also normally distributed: this can be checked with histograms nad Q-Q plots

![image](https://editor.analyticsvidhya.com/uploads/79532normality%20of%20error.png)

- No autocorrelation: error terms should be independent of each other - this can be tested with the Durbin Watson test, where the null hypothesis assumes there is no autocorrelation

![image](https://editor.analyticsvidhya.com/uploads/38946DW.png)

There are also a few evaluation metrics for regression:
- R^2 aka the "coefficient of determination": the most common metric, is the ratio of variation to the total variation (equation below - SS_res is the residual sum of squares and SS_tot is the total sum of squares). The value will be between 0 and 1; the closer to 1, the better the model. However, as the number of features increases, the value of R^2 increases and gives the (sometiems false) illusion of a good model.

![image](https://editor.analyticsvidhya.com/uploads/74264r2.png)

- Adjusted R^2: improvement to R^2, only considers features that are important for the model and shows the real improvement of the model. The equation is detailed below

![image](https://editor.analyticsvidhya.com/uploads/80741adjusted%20r2.png)

- Mean Squared Error (MSE)

![image](https://editor.analyticsvidhya.com/uploads/42113mse.jpg)

- Root Mean Squared Error (RMSE): root of the mean difference between actual and predicted values. It penalizes large errors

![image](https://editor.analyticsvidhya.com/uploads/69457rmse.png)


This was heavily baesd on [this article](https://www.analyticsvidhya.com/blog/2021/05/all-you-need-to-know-about-your-first-machine-learning-model-linear-regression/).
