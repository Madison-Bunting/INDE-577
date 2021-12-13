# Unsupervised Learning

![image](https://user-images.githubusercontent.com/89811204/132997444-5ef28bd9-c01b-4d7e-b0f4-3c74b87dfae2.png)

Unsupervised learning is used to find underlying patterns in data, and involves finding structures and relationships from inputs. This is helpful when we have unlabeled data or aren't sure which outputs are meaningful. There is a set of data that is **unlabeled** to learn from, with the goal of identifying patterns in that data. In contrast to supervised learning, which focuses on labels, unspervised learning focuses on **features** of the data. 

The result of an unsupervised learning model is to place observations into specific clusters (clustering), or to create rules to identify associations between variables (association). With large datasets, it is important to keep the datasets used for training as small and efficient as possible. Unsupervised learning algorithms are also able to utilize "dimensionality reduction" to represent the information in a dataset with only a portion of the actual content. Unsupervised learningallows you to perform more complex processing tasks compared to supervised learning, and is in some ways more powerful because it can identify patterns within a dataset not visible to a human observer, but it can be more unpredictable compared with other deep learning and reinforcement learning methods. 

Variables:
- features

Types of Algorithms:
- **Dimensionality Reduction**
  - goal: combine parts of data in unique ways to convey meaning in less space
  - e.g. analyzing high resolution images by reducing the resolution an appropriate amount
  - common algorithms: principal component analysis (PCA), singular-value decomposition (SVD)
- **Clustering**
  - goal: find similarities/patterns in observed data and put them into "clusters" or subgroups hat are as similar to others within the group and as different from data in other clusters as possible
  - e.g. detecting groups of similar visitors to a blog (40% male comic book lovers who read in the evening vs 20% young sci-fi lovers who visit on weekends)
  - common algorithms: K-means clustering, hierarchical clustering, probalistic clustering
- **Association**
  - goal: dentify sequences and new and interesting insights between different objects in a set. In this case, the pattern identified is a rule (like if *this* then *that*)
  - e.g. analyzing supermarket data and finding that people who buy bbq sauce and potato chips tend to also buy steak
  - common algorithms: Apriori algorithm, frequent pattern (FP) growth algorithm, rapid association rule mining (RARM), ECLAT algorithm

List of unsupervised learning algorithms in this repository:
  - [K-Means Clustering](https://github.com/Madison-Bunting/INDE-577/tree/main/unsupervised%20learning/1%20-%20means%20clustering)
  - [Principle Component Analysis](https://github.com/Madison-Bunting/INDE-577/tree/main/unsupervised%20learning/2%20-%20principle%20component%20analysis)
