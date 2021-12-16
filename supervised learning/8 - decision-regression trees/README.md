# Decision Trees

![image](https://i1.wp.com/dataaspirant.com/wp-content/uploads/2017/01/B03905_05_01-compressor.png?resize=1024%2C566&ssl=1)

This algorithm can be used for both classification and regression problems. It uses the analogy of a tree. Each _internal node_ corresponds to an attribute of the data, and each _leaf node_ corresponds to a class label.

Algorithm:
1. Place the best attribute of the dataset at the _root_ of the tree.
   - Compare the values of the root attribute with the record's attribute, then follow the branch corresponding to that value and jump to the next node using the **Sum of Product representation (or Disjunctive Normal Form)**. For a class, every branch from the root of the tree to a leaf node having the same class is a conjunction (product) of values, different branches ending in that class form disjunction (sum).
2. Split training set into _subsets_ in such a way that each subset contains data with the same value for an attribute.
3. Repeat 1-2 on each subset until you find _leaf nodes_ in all the branches of the tree.
   - Compare the record's attribute values with other internal nodes of the tree until we reach a leaf node with the predicted class value 
   - The primary challenge is to determine which attributes should be considered at each level. There are a couple popular attribute selection measures:
     - Entropy (Information gain)
       - Assume attributes are categorical and try to estimate the information contained by each attribute
       - Entropy is the measure of randomness or uncertainty of a random variable X. In a binary classification problem, if all examples are positive or all are negative, entropy will be 0 (i.e. low). If half the records are of positive class and half are of negative class, entropy is 1 (i.e. high). The equation for the *entropy measure* is below

![image](https://user-images.githubusercontent.com/89811204/146313029-48b75b32-2fc3-4376-8f82-898d03642e6d.png)

   - Gini index
      - Assume attributes are continuous, the index is a metric that measures how often a randomly chosen element would be inorrectly identified. Thus, we prefer a low gini index

There are a few assumptions with the training set: 
- At the beginning, the root is the whole training set
- Feature values are preferred to be categorical. If the values are continuous, they are discretized prior to building the model. 
- Records are distributed recursively on the basis of attribute values
- Order to placing attributes as root or internal node of the tree is done using some statistical approach

Overfitting is a common issue with decision trees. There are two approaches to avoid this:
- Pre-Pruning
  - Stops the tree construction early. It is preferred not to split a node it its goodness measure is below a threshhold, but it's difficult to choose a stopping point
- Post-pruning
  - Build a complete tree. If the tree demonstrates overfitting, then prune using cross-validation data to check the effect. The cross validation data tests whether expanding a node will make an improvement (increase in accuracy) or not

The above is heavily based on [this article](https://dataaspirant.com/how-decision-tree-algorithm-works/), which can be referenced for further information.
