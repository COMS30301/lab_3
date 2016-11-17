# Lab 3: Choice of learning algorithm (Scikit-Learn)

The aim of this exercise is to go through the Lab 2 this time using Python and its machine learning library *Scikit-Learn*. During this lab you will learn Python’s interactive interface: *Jupyter Notebook*.

We will have to solve the two classification problems from Lab 2, with the following training sets:

*   The **mystery** dataset (`mystery.csv`).
*   The **shooting** dataset (`shooting.csv`).

This time the datasets are in *Comma Separated Values* format. There are no testing sets, so to assess performance, please use [10-fold cross-validation](http://scikit-learn.org/stable/modules/cross_validation.html#k-fold).

You will compare performance of two subsymbolic classifiers:

*   Nearest Neighbour - to classify a new instance, it looks for the most similar instance in the training set (with the shortest Euclidian distance), and assigns the class of this closest instance. This classifier is implemented in Scikit-Learn in [`sklearn.neighbors.NearestNeighbors`](http://scikit-learn.org/stable/modules/neighbors.html)
*   Perceptron - this classifier simply finds a line (note: line, not curve) in two-dimensional feature space which most accurately divides instances from the training set in two classes. During classification, it simply checks on which side of the line a new instance lies. To generate this “Perceptron” classifier in Scikit-Learn, we will use: [`sklearn.linear_model.Perceptron`](http://scikit-learn.org/stable/modules/linear_model.html#perceptron)

First, find the accuracy of the above classifiers on the the above data sets (percentage of Correctly Classified Instances in [Stratified cross-validation](http://scikit-learn.org/stable/modules/generated/sklearn.cross_validation.StratifiedKFold.html). Can you say that one of the above algorithms is in general better than the other?

Importantly, **explain why certain algorithm was more accurate than the other**. To understand the result you just got, visualize the two data sets with Python’s [matplotlib](http://matplotlib.org/) plotting package.  
The skeleton Jupyter Notebook is available here: `Lab3.ipynb`. To run it just do:

    jupyter notebook

... in the folder where you downloaded both datasets and the skeleton code.

## Useful links

*   [SVM](http://scikit-learn.org/stable/auto_examples/svm/plot_svm_margin.html)
*   [kNN](http://scikit-learn.org/stable/auto_examples/neighbors/plot_classification.html#example-neighbors-plot-classification-py)
*   [Perceptron 1](http://scikit-learn.org/stable/modules/linear_model.html#perceptron)
*   [Perceptron 2](http://stamfordresearch.com/python-perceptron-re-visited/)
