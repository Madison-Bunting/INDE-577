# K-Means Clustering Algorithm

ch 9
https://github.com/ageron/handson-ml2/blob/master/09_unsupervised_learning.ipynb
intro to statistical machine learning ch 10.3

![image](https://user-images.githubusercontent.com/89811204/132998743-c4e77461-5a13-4670-b59d-40d26ee91033.png)

## What is K-Means Clustering?
In the k-means clustering algorithm, we group the data in to k groups, or clusters, such that all the data points in the same cluster are as similar to each other as possible. The data points that augment the clusters are visibly different from those points. Points cana only belong to one group.

To calculate the simimlarity between data points, we use distances like Euclidean distance as a reference. Each group has a centroid (central point) and they are thought of as teh representative of the group.
 
## How does K-Means Clustering work?
1. Choose the number of clusters, k
2. Select k random points from the data as centroids. Calculate the Eucledean Distance from each feature vector to each centroid.
![image](https://user-images.githubusercontent.com/89811204/132998845-37a6f436-47b4-4337-a030-72bd9212d59f.png)

4. We next update the centroids in clusters
5. Report previous steps 3-4 until convergence is reached (no change in the centroids)
