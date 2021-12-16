# Ensemble Learning (Random Forests)

Ensemble learning is a model that makes predictions based on a number of different models. Combining individual models makes ensemble models more flexible (less bias) and less data-sensitive (less variance).

The two most popular ensemble methods are:
  - Bootstrapping: Training a bunch of individual models in a parallel way. Each model is trained by a random subset of the data
  - Bagging: Training a bunch of individual models in a sequential way. Each individual model learns from mistakes made by the previous model.

![image](https://miro.medium.com/max/2000/1*bUySDOFp1SdzJXWmWJsXRQ.png)

A single decision tree is easy to conceptualize, but typically suffers from high variance, which usually means they are not competitive with other models in terms of accuracy. One way to overcome this limitation is to produce many variants of a single decision tree by selecting every time a different subset of the same training set in the context of randomization-based ensemble methods.

![image](https://miro.medium.com/max/2000/1*jXkT3mj1mCqMaX5SqU1wNw.png)

Random forest is a machine learning algorithm based on decision trees, which below the a class of machine learning algorithms called **ensemble methods**. Random trees can handle a mix of categorical and numerical variables, and is less sensitive to scaling and is computationally less intensive than SVM. Random trees also provide an effective way of handling missing data and are less sensitive to overfitting without needing hyperparameter tuning.

Algorithm
1. Select n (e.g. 1000) random subsets from the training set
2. Train n (e.g. 1000) decision trees
   - one random subset is used to train one decisions tree
   - the optimal splits for each decision tree are based on a random subset of features (e.g. 10 features in total, randomly select 5 out of 10 features to split)
 3. Each individual tree predicts the records/candidates in the test set, independently
 4. Make the final prediction
    - For each candidate in teh test set, random forest uses the class (e.g. cat or dog) with the majority fove as this candidate's final prediction

The fundamental principle of ensemble methods is based on randomization. There are three main decisions to make when constructing a tree:
- method for splitting the leaves
- type of predictor used in each leaf
- method for injecting randomness into the tree (bagging or bootstrapping)

There are a few stopping criteria:
- minimum number of samples in a terminal node to allow it to split
- minimum number of samples in a leaf node when the terminal node is split
- maximum tree depth, i.e. the maximum number of levels a tree can grow
- Tree accuracy (defined by the Gini Index) is less than a fixed threshold


The above information is largely based on [this article](https://towardsdatascience.com/basic-ensemble-learning-random-forest-adaboost-gradient-boosting-step-by-step-explained-95d49d1e2725), which can be referenced for additional information.
