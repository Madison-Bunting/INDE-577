# Perceptron

![image](https://qph.fs.quoracdn.net/main-qimg-903a35d8c93d2009fea2118c37a69f13-pjlq)

The [Perceptron](https://en.wikipedia.org/wiki/Perceptron) is a supervised, single layer neural network binary linear classifier. Simply, it can be thought of as a mathematical model that draws a boundary to separate two groups in space. It was developed by Frank Rosenblatt in 195y at the Corenll Aeronautical Laboratory, funded by the United States Office of Naval Research. Single-layer perceptrons can be combined together into a [Multi-Layer Perceptron (MLP)](https://github.com/Madison-Bunting/INDE-577/tree/main/supervised%20learning/4%20-%20neural%20networks)
- Linear classifier: training data should be classified into corresponding categories (i.e. if there are two categories, all the training data must lie in those two categories)
- Binary classifier: defines that there should only be two categories

Perceptrons are trained in three phases:

**1. Data Processing**

  As a binary classifier, perceptrons are meant to classify input into two groups: yes/no, black/white, up/down, etc, corresponding to 1/0 or 1/-1 outputs (depending on the selected activation function). To prepare data, we must first determine the two output groups and classify data in numerical terms, at which point the data will be in a format that will allow the perceptron to be trained. 
  
**2. Predict Results**

![image](https://akashsethi24.files.wordpress.com/2017/09/perceptron1.png?resize=529%2C347)

The perceptron learning rule states that the algorithm would automatically learn the optimal weight coefficients. The input features are then multiplied with these weights in a weighted sum to determine if the neuron "fires" or not (returns 1 if positive, 0 otherwise, or 1 and -1).

![image](https://user-images.githubusercontent.com/89811204/146212310-d319e5d3-7cf9-4ef6-9525-7114c1f8db4c.png)

In the equation above:
- w: vector of real valued weights
- b: bias (an element that adjusts the boundary away from the origin without any dependence on the input value
- x: vector of input values

![image](https://user-images.githubusercontent.com/89811204/146212640-e65cef67-2d62-4d45-9245-3239cde4d8c6.png)

- m: number of inputs to the percpetron

![image](https://www.simplilearn.com/ice9/free_resources_article_thumb/Perceptron/Perceptron_17.jpg)

Choose an activation function

![image](https://www.simplilearn.com/ice9/free_resources_article_thumb/Perceptron/Perceptron_9.jpg)

- [Heaviside step function](https://en.wikipedia.org/wiki/Heaviside_step_function): triggered above a certain value of neuron output; otherwise it outputs zero
- Sign function: outputs +1 or -1 depending whether the neuron output is greater than 0 or not
- Sigmoid: S-curve that outputs a value between 0 and 1

**3. Update Weights**

The goal is to reduce the number of misclassified points, so by iterating through the algorithm, the separation line moves in space and after a few epochs, the algorithm classifies it correctly.

In the Perceptron learnning rule, predicted output is compared with known output; if they do not match, error is propagated backward to allow weight adjustment to happen

The above information was based on [this article](https://www.simplilearn.com/ice9/free_resources_article_thumb/Perceptron/Perceptron_36.jpg), which can be referenced for further reading.
