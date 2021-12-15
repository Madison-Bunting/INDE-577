# Stochastic Gradient Descent
Ch 4 p173
https://github.com/ageron/handson-ml2/blob/master/04_training_linear_models.ipynb
https://scikit-learn.org/stable/modules/sgd.html#sgd
deep learning illustrated textbook
python machine learning pg 64 in pdf
http://localhost:8888/notebooks/OneDrive/Documents/Rice/Fall%202021/INDE%20577/lecture%204%20-%20gradient%20descent%20and%20neural%20networks%20pt%200.ipynb


When there are one or more inputs you can use a process of optimizing the values of the coefficients by iteratively minimizing the error of the model on your training data.

This operation is called Gradient Descent and works by starting with random values for each coefficient. The sum of the squared errors are calculated for each pair of input and output values. A learning rate is used as a scale factor and the coefficients are updated in the direction towards minimizing the error. The process is repeated until a minimum sum squared error is achieved or no further improvement is possible.

When using this method, you must select a learning rate (alpha) parameter that determines the size of the improvement step to take on each iteration of the procedure.

Gradient descent is often taught using a linear regression model because it is relatively straightforward to understand. In practice, it is useful when you have a very large dataset either in the number of rows or the number of columns that may not fit into memory.
