### Support Vector Machine

##### Idea (for classify two clusters of points): find the optimal hyperplane that maximizes the margin between two data classes using gradient descent.

##### Usage: 

- Classification
- Regression (Time series predictions, etc)
- Outlier detection
- Clustering

##### Examples

- [Use Scikit-learn's SVM function to classify images in mnist](https://github.com/ksopyla/svm_mnist_digit_classification)
- [Pulse classification](https://github.com/akasantony/pulse-classification-svm)

SVM is great when we have relatively small dataset. Other algorithms like deep neural network and random forest need more data. The decision of which classifier to use depends on your dataset and the general complexity of the problem. "Premature optimization is the root of all evil (or at least most of it) in programming."


It's a supervised machine learning algorithm which can be used for both classification or regression problems. But it's usually used for classification. Given 2 or more labeled classes of data, it acts as a discriminative classifier, formally defined by an optimal hyperplane that seperates all the classes. New examples that are then mapped into that same space can be categorized based on on which side of the gap they fall.


Optimization: maximize the margin between classes. (Points lie on the margin edges of the decision boundary are called support vectors.)


Hyperplane: decision surface. Obviously a hyperplane is a binary classifier.


Machine Learning in general is to approximate a function or mapping from the input space to the output space.


Loss function for classification of points (what to minimize); Objective function (what to optimize).

- Loss function:

We will use the Hinge loss. This is a loss function used for training classifier. The hinge loss is used for "maximum-margin" classification, most notably for support vector machines (SVMs).

```
c(x, y, f(x)) = 0 if y*f(x) >= 1
else 1 - y*f(x)
```
where `c` is the loss function, `x` the sample, `y` is the true label.