# Neive Bayes Classifier

![image](https://user-images.githubusercontent.com/89811204/146295580-8a329483-1f0b-4749-a607-03c67172d7f1.png)

Naive Bayes is based on Bayes Theorem, a mathematical formula popularized by Reverend Thomas Bayes in the 1760s that determines the conditional probability of an event, based on prior knowledge of conditions that might be related to the event.  It is called "naive" because the classifier assumes that the input features to the model are independent of each other, meaning it assumes that changing one input feature will not affect any of the others, even though this is often not the case with datasets. 

**Applications:**
- real-time prediction
- multi-class prediction
- text classification/spam filtering/sentiment analysis
- recommenation systems

Naive Bayes has an advantage over algorithms like SVM and Ensemble because of its probablistic approach: all computations are done in real time and the outputs are generated instantaneously.

Bayes Rule is represented by the following algorithm (also at the top of this page):
P(A|B) = (P(B|A) * P(A)) / P(B). This tells us how often A happens *given that* B happens, when we know how often B happens *given that* A happens, how likely A is on its own, and how likely B is on its own.

There are three main types of classifiers:
- **Gaussian Naive Bayes**: used when the values of predictors are continuous in nature and it is assumed that they follow Gaussian (normal) distribution
- **Bermoulli Naive Bayes**: used when the predictors are boolean/binary in nautre and it is assumed they follow Bernoulli distribution
- **Multinomial Naive Bayes**: uses multinomimal distribution and is used when features represent frequency of something occurring, like the number of words in a document or text classification purposes

The above is largely based on [this article](https://medium.datadriveninvestor.com/what-are-naive-bayes-classifiers-dd8bc49db817), which can be referenced for additional information.
