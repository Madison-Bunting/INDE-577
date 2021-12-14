# K-Means Clustering Algorithm

ch 9
https://github.com/ageron/handson-ml2/blob/master/09_unsupervised_learning.ipynb
intro to statistical machine learning ch 10.3
python machine learning ch 11
https://github.com/rasbt/python-machine-learning-book-3rd-edition/tree/master/ch11
http://localhost:8888/notebooks/OneDrive/Documents/Rice/Fall%202021/INDE%20577/10%20-%20K%20means%20clustering.ipynb

![image](https://user-images.githubusercontent.com/89811204/132998743-c4e77461-5a13-4670-b59d-40d26ee91033.png)

## What is K-Means Clustering?
K-means clustering is one of the most popular unsupervised machine learning algorithms. The objective of the algorithm is to group datapoints with certain similarities together into **clusters** to find underlying patterns. K-means clustering does this by looking for a pre-set number (k) of clusters in that dataset. Points are only able to be part of one cluster, and each cluster has a "centroid" that roughly averages the data and represents the center of the cluster. Data points are then allocated to each of the clusters by assigning them to clusters in such a way that minimizes each cluster's sum of squares (often using Euclidean distance).

At a high level, the algorithm starts with a set of k randomly selected centroids, then iteratively optimizes the locations of those centroids until there is effectively no change in the centroids between iterations (meaning the clustering was successful) or the algorithm has completed the defined number of iterations.
 
## How does K-Means Clustering work?
1. Choose the number of clusters, k
2. Select k random points from the data as centroids. Calculate the Eucledean Distance from each feature vector to each centroid.
![image](https://user-images.githubusercontent.com/89811204/132998845-37a6f436-47b4-4337-a030-72bd9212d59f.png)

4. Update the centroid for each cluster.
5. Report previous steps 3-4 until the centroides converge (no change in cetnroids) or the algorithm reaches the maximum number of iterations.
