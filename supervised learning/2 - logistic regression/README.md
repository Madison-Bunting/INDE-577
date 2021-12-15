# Logistic Regression

![image](https://miro.medium.com/max/1050/1*dm6ZaX5fuSmuVvM4Ds-vcg.jpeg)

Logistic Regression is a machine learning algorithm commonly used for classification problems, but is a predictive analysis algorithm based on the probabilistic framework called [maximum likelihood estimation](https://towardsdatascience.com/an-introduction-to-logistic-regression-8136ad65da2e).

There are two primary types of logistic regression:
- Binary (e.g. determine whether a tumor is malignant or benign, or if a person will default on a bank loan)
- Multi-linear functions that predict class labels (e.g. is the information describing a cat, dog, or a sheep)

It is similar to Linear Regression, but it results in a more complex function, the **sigmoid function**.

![image](https://miro.medium.com/max/960/1*OUOB_YF41M-O4GgZH_F2rw.png)

By rule of thumb, if the predicted probability is greater than or equal to 0.5, it is likely the bank loan applicant will default.

Cost Function:

![image](https://miro.medium.com/max/1050/1*2g14OVjyJqio2zXwJxgj2w.png)


Graph of logistic regression

![image](https://user-images.githubusercontent.com/89811204/146216534-9a601761-bf94-489a-a64e-4bd363545ba0.png)

The above two cost functions can be combined into a single function

![image](https://miro.medium.com/max/1400/1*_52kKSp8zWgVTNtnE2eYrg.png)

Logistic Regression models make a few assumptions:
- the dependent variable is binary, multinomial, or ordinal
- observations are independent (not from repeated measurements)
- little to no collinearity among the independent variables
- linearity of independent variables and log odds
- The success of the model depends on the sample size (usually requiring large sample sizes to achieve high accuracy)

The above is largely based on [this article](https://towardsdatascience.com/an-introduction-to-logistic-regression-8136ad65da2e), which can be referenced for additional information.
