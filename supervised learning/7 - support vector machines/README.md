# Support Vector Machines (SVM)

Support Vector Machines are statistical learning frameworks first developed at AT&T Bell Laboratories by Vladimir Vapnik. In short, SVM finds a hyper-plane in N-dimensional space (N = number of features) that creates a boundary between the types of data. Thus, it can only perform binary classification, but there are various techniques for multi-class problems. It works very well for linearly separable data. We use **Kernalized SVM** for non-linearly separable data. SVM is more often used for classification, but it can also be used for regression. It is preferred by many due to its significant accuracy with less computational power.

![image](https://user-images.githubusercontent.com/89811204/146305295-51212e92-0403-4d8c-bc1d-500800f1c502.png)

**Linear SVM**
This algorithm separates the data with a straight line. There are two different kinds of margins:
- Hard-margin: If the data is linearly separable, a line can be drawn which maximizes the distance between itself and the nearest datapoints on either side
- Soft-margin: Allows for a balance between violations where a feature vector falls within the margins of the hyperplane. This model is less sensitive to outliers, which would force the hard margin to compensate. When using scikitlearn, this is the "c" parameter.

Algorithm:
- Plot each datapoint in an N-dimensional space, where N is the number of features/attributes in the data
- Find the optimal hyperplane to separate the data
  - Use the **support vectors** to do this. Support vectors are datapoints closer to the hyperplate that influence the position and orientation of the hyperplane - we can use these support vectors to maximize the margin of the classifier. Deleting them changes the position of the hyperplane.

![image](https://miro.medium.com/max/1050/0*ecA4Ls8kBYSM5nza.jpg)

- Weights update function (using gradients)

![image](https://miro.medium.com/max/1050/1*WUphtYLfTOAoaXQXvImBeA.png)

which becomes

![image](https://miro.medium.com/max/462/1*-nKEXrWos8Iuf-DWSv_srQ.png)

for when there is *no misclassification* (i.e. our model correctly predicts the class of our datapoint, so we only have to update the gradient from the regularization parameter), and 

![image](https://miro.medium.com/max/642/1*tnvMhAKaTUCO43diEvtTAQ.png)

when there has been a *misclassification* (i.e. the model made a mistake on the prediction of the class of a datapoint, so we need to include the loss along with the regularization parameter to perform the gradient update).

- Take the output of the linear function: if the output is larger than 1, we identify it with one class, if the output is -1, we identify it with another class. 

Cost function: our goal is to maximize the margin between datapoints and the hyperplane, so we use hinge loss (below: piecewise function (left), function (right))

![image](https://miro.medium.com/max/1624/1*hHlytjVk6d7O2WWvG2Gdig.png)

Final cost function:

![image](https://miro.medium.com/max/1400/1*GQAd28bK8LKOL2kOOFY-tg.png)

**Kernelized SVM**

This method allows a nonlinear function to separate the dataset. It maps each datapoint into a higher dimension, exemplified below:

![image](https://miro.medium.com/max/1400/1*ZpkLQf2FNfzfH4HXeMw4MQ.png)

- kernel: measure of similarity between datapoints
- kernel function: reveals the similarity between two datapoints in the newly transformed feature space. There are a few kernel function options:
  - **Redial Basis Function Kernel (RBF):** The similariy between two points in the transformed feature space is an exponentially decaying function of the distance between the vectors and the original input space. RBF is the default kernel used in SVM

![image](https://user-images.githubusercontent.com/89811204/146305418-93423376-1086-4f5f-a0e9-9c099d7c3132.png)

  - **Polynomial Kernel:** takes an additional parameter, "degree" that controls the model's complexity and computational cost of the transformation
  - **Kernel Trick:** the actual transformation of points to the new high dimensional space is not always necessary. Though the trick itself is quite complex, simply explained, the kernelized SVM can internally compute these complex transformations just in terms of similarity calculations between pairs of points in the higher dimensional feature space where the transformed feature representation is implicit. This similarity function, which is mathematically a kind of complex dot product is actually the kernel of a kernelized SVM. This makes it practical to apply SVM, when the underlying feature space is complex, or even infinite-dimensional.

The above information is largely based on [this article](https://towardsdatascience.com/support-vector-machine-introduction-to-machine-learning-algorithms-934a444fca47), which can be reference for additional information.
