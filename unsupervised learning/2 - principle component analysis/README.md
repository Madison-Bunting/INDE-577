# Principle Component Analysis (PCA)

![image](https://miro.medium.com/max/2158/0*5Iaw94wlYCTp0GuK.png)

Principle component analysis was invented at the beginning of hte 20th centry but Karl Pearson, and is analogous to the principal axis theorem in mechanics. Principle Component Analysis is a dimension-reduciton tool that can be used to reduce a large set of variables into a smaller set that still contains the majority of the information from the larger set. For example, making a 3D set of data into a 2D set of data, as shown above.

PCA is useful because it can reduce the size of the dataset (therefore decreasing the amount of time it takes algorithms to run), better visualize datasets in fewer dimensions, maximizes variance, reduces overfitting, etc.

If all the features in a dataset were completely independent, PCA's task would be difficult. However, there are often redundancies, including features that are indicators of a signal humans haven't observed yet, but that PCA can help reveal (hence why PCA is an example of unsupervised learning). For a simple explanation of how PCA works, observe the simple dataset and its line of best fit below:

![image](https://user-images.githubusercontent.com/89811204/146057577-c1b0197a-a4ad-49f9-8f77-839dc8674ea0.png)

Because of this, it would be possible to reorient the x and y axes such that the origin is centered on the data and parallel to the line of best fit.

![image](https://miro.medium.com/max/2000/0*e9szS2xre3rEkF8F.png)

Each datapoint can then be projected onto the primary axis (line of best fit)

![image](https://user-images.githubusercontent.com/89811204/146060161-2c587d73-9897-4850-95c1-691f97160d88.png)

The 2D dataset has now been compressed onto a 1D line, and only one relevant dimension remains, so the second axis can be discarded.

![image](https://user-images.githubusercontent.com/89811204/146060065-b4cf8618-6efe-4a11-aafb-bc51ba892ab7.png)

Compared with the original dataset, one can observe that it is not an exact representation of the data, but it does capture the original data's essence. Looking at the data again, you might ask: why did we decide to collapse the data along the longer line instead of the shorter one?

![image](https://miro.medium.com/max/1050/0*jhA5DRdruIePMouc.png)

It turns out, the vector capable of capturing the maximum variance of the data minimizes the distance required to move the data as a projection onto the vector.

A more complicated defition of PCA would be that it is an orthogonal transformation that takes the data to a new coordinate system such that the greatest variance by some scalar projection of the data comes to lie on the first coordinate (the first principal component), the second greatest variance comes to lie on the second coordinate, etc.

The math underlying PCA is quite complicated, but at a high level:
Consider an n x p data matrix X, where each of the rows represents a different repetition of the experiment and each of the columns gives a particular kind of feature. the k-th component can be found by subtracting the first k principal components from X as shown below:

![image](https://user-images.githubusercontent.com/89811204/146064331-67d84e5c-b938-40f7-9fc1-716577c032cb.png)

then finding a new weight vector which extracts the maximum variance from this new data matrix, as detailed below:

![image](https://user-images.githubusercontent.com/89811204/146064425-486393f3-b30f-4de9-abb8-2db1c72dc636.png)

i.e. the weight vectors are the eigenvectors of X^TX. The full principal components of X can therefore be given as T = XW, where W is a p by p matrix of weights whos colums are the eigenvectors fo X^TX.


This explanation was heavily based on [this article from Medium](https://medium.com/@mallrishabh52/principal-components-analysis-7f6ff559cd83) and [this article from Wikipedia](https://en.wikipedia.org/wiki/Principal_component_analysis). 
