# Gradient Descent

![image](https://camo.githubusercontent.com/fc6bcb573c00619457b2b886dddc8322402c66ccec48bc82ac35cf1de0c95a43/68747470733a2f2f692e696d6775722e636f6d2f786e5076456f6b2e676966)

Gradient descent is an optimization algorithm to find a local minimum of a differentiable function. It is most often used to find coefficient values that minimize a cost function. 

Imagine you are hiking down into a valley, and this is its topographical map (where lines that are closer together indicate the slope of the valley is steeper between them). In the case below, the valley gets less steep the lower you hike, meaning the reduced gradient correlates with a reduced slope and step size for the hiker.

![image](https://machinelearningmastery.com/wp-content/uploads/2021/07/gradientDescent1.png)

Let's say you want to reach the bottom of the valley the fastest. You look around and realize there are several options of paths to take... but how do you know which is the best? This is where the concept of a [gradient](https://www.khanacademy.org/math/multivariable-calculus/multivariable-derivatives/v/gradient?modal=1) comes in handy. Simply put, the gradient is the slop of a function; it is the derivative of a function with more than one input variable and measures the change in all weights with regard to the change in error. 

The equation below characterises this relationship: 
- b is the next position of the hiker
- a is their current position
- "-" is what makes it gradient _descent_
- the gradient term (delta f(a)) is the direction of the steepest descent

The function initializes at a given point, then iteratively takes steps in the direction of steepest descent. The size of the steps is called the **learning rate**, larger learning rates can cause the algorithm to skip around and potentially miss the local minimum (as seen below), while small learning rates follow the curve of the function.

![image](https://github.com/Carmichael89/Machine-Learning-and-Data-Analytics/raw/4106b4cccf960f70dbf06ca8a531e4c2d8b92e4e/Gradient%20Descent/GradientDescentMultiAlpha.png)

At each iteration, the changes in weights cause a small shift in the line towards its best representation:

![image](https://miro.medium.com/max/648/1*1mwtcdCPw0eQbpUkus8vwA.gif)

There are two main types of gradient descent, both of which are programmed from scratch in the [accompanying notebook](https://github.com/Madison-Bunting/INDE-577/blob/main/supervised%20learning/1%20-%20gradient%20descent/Gradient%20Descent%20-%20from%20scratch.ipynb):
- **Batch Gradient Descent** (aka vanilla gradient descent)
  - calculates the error for each example within the training dataset, but the model is only updated after all training examples have been updated
  - the whole process is called a "training epoch"
  - Advantages: model is computationally efficient, produces stable error gradient, and a stable convergence
  - Disadvantages: stable error gradient can sometimes result in sub-optimal convergence. It also requires the entire training set to be in memory and available to the algorithm

- **Stochastic Gradient Descent**
  - updates the parameters for each training example one by one
  - depending on the problem, this can make it faster than batch gradient descent
  - Advantage: frequent updates allow for a detailed rate of improvement
  - Disadvantage: frequent updates are more computationally expensive and can result in noisy gradients, which can result in an error graph with spikes rather than steady decrease

When there are one or more inputs you can use a process of optimizing the values of the coefficients by iteratively minimizing the error of the model on your training data.

Mean squared error is a common measure of performance:

![image](https://miro.medium.com/max/1013/1*GQ6vjZ9j0K5V7BReHywWAA.png)

Check out [this video](https://youtu.be/IHZwWFHWa-w?t=416) for more information.
