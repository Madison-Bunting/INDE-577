# K Nearest Neighbors (KNN)

![image](https://d2908q01vomqb2.cloudfront.net/f1f836cb4ea6efb2a0b1b99f41ad8b103eff4b59/2018/07/11/sagemaker-knn-1.gif)
Note: KNN Classification (left), KNN Regression (right)


K Nearest Neighbors is a simple algorithm that stores all the available cases and classifies new data/case based on a similarity measure. It is mostly used to classify a datapoint based on how its neighbors are classified. This method is used in areas from recommendation systems to anomaly detection to image/text classification. KNN can also be used for regression, though this application is less common than classification. 

Classification
In short, KNN essentially boils down to forming a majority vote between K most similar (i.e. closest) instances to a given "unseen" observation. 

![image](http://res.cloudinary.com/dyd911kmh/image/upload/f_auto,q_auto:best/v1531424125/KNN_final1_ibdm8a.png)

Generalized Algorithm: 
1. Load training and testing datasets
2. Specify/choose the value of k
   - There is no set method for doing this. Often, you can plot various values using trail and error, assuming the training data was unknown. Note that smaller values for K can be noisy and will have a higher influence on the result, while larger values of K will have smoother decision boundaries (meaning lower variance but increased bias... and are computationally expensive). 
   - Alternatively, you can use cross validation: select a cross-validation dataset from the training dataset. Take a small portion from the training dataset and call it a "validation" dataset, then use the same value to evaluate different possible values of K, i.e. predict the label for every instance in the validation set using K = 1, K = 2, K = 3..., then look at which value of K gives the best performance on the validation set and use that value as the final seting.
   - In general, choosing the value of k is k = sqrt(N), where N is the number of samples in the training dataset
   - Try to keep the value of k odd to avoid confusion between two classes of data
4. For each point in the test data:
   a. Calculate the distance between the point and each point in the dataset ([Euclidean](https://en.wikipedia.org/wiki/Euclidean_distance), [Manhattan](https://en.wikipedia.org/wiki/Taxicab_geometry), and [Minkowski](https://en.wikipedia.org/wiki/Minkowski_distance) istance methods are common metrics for this). Note that all of these algorithms are only valid for continuous variables; [Hamming distance](https://en.wikipedia.org/wiki/Hamming_distance) must be used for categorical variables
   
   ![image](https://www.saedsayad.com/images/KNN_similarity.png)
   
   b. Sort the values in ascending order based on distances
   c. Find the top k values from the sorted list
   d. Find the frequency (statistical [mode](https://en.wikipedia.org/wiki/Mode_(statistics)) of the labels of the top k values
   e. Assign the mode to the test data point
   f. The assigned value is the classified (classification) or predicted (regression) value for that particular datapoint.

The above is largely based on [this article](https://towardsdatascience.com/a-simple-introduction-to-k-nearest-neighbors-algorithm-b3519ed98e), which can be referenced for additional information.
