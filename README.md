# SVM

## Problem Statement

**Salary Data :**

Prepare a classification model using SVM for salary data

**Forest Fires :**

classify the Size_Categorie using SVM

# ➳ Support Vector Machine (SVM)

![SVM Title](https://github.com/yagniksorathiya/SVM/assets/129974278/5ecdb0ff-adfd-453b-a0d2-37663fd3850b)

Support Vector Machines (SVMs) are a powerful and versatile machine learning algorithm that has gained widespread popularity among data scientists in recent years. SVMs are widely used for classification, regression, and outlier detection (one-class SVM), and have proven to be highly effective in solving complex problems in various fields, including **computer vision** (image classification, object detection, etc.), **natural language processing** (sentiment analysis, text classification, etc.), and **bioinformatics** (gene expression analysis, protein classification, disease diagnosis, etc.).

## ↳ What is Support Vector Machine (SVM)?

Support Vector Machine or SVM is one of the most popular **Supervised Learning algorithms**, which is used for Classification as well as **Regression problems**. However, primarily, it is used for Classification problems in Machine Learning.

The goal of the SVM algorithm is to create the best line or decision boundary that can segregate n-dimensional space into classes so that we can easily put the new data point in the correct category in the future. This best decision boundary is called a **hyperplane**.

SVM chooses the extreme points/vectors that help in creating the hyperplane. These extreme cases are called as **support vectors**, and hence algorithm is termed as Support Vector Machine. Consider the below diagram in which there are two different categories that are classified using a decision boundary or hyperplane:

![SVM-algorithmvisual-representation](https://github.com/yagniksorathiya/SVM/assets/129974278/b71ee4e7-a2e5-451b-b5c0-32ae07d11733)

SVM algorithm can be used for **Face detection, image classification, text categorization, etc.**

**Advantages of SVM**

+ Effective in high dimensional spaces

+ Still effective in cases where the number of dimensions is greater than the number of samples

+ Uses a subset of training points in the decision function that makes it memory efficient

+ Different kernel functions can be specified for the decision function that also makes it versatile

**Disadvantages of SVM**

+ If the number of features is much larger than the number of samples, avoid over-fitting in choosing kernel functions and regularization term is crucial.

+ SVMs do not directly provide probability estimates, these are calculated using five-fold cross-validation

## ↳ Types of SVM

**SVM can be of two types:**

**Linear SVM:** Linear SVM is used for linearly separable data, which means if a dataset can be classified into two classes by using a single straight line, then such data is termed as linearly separable data, and classifier is used called as Linear SVM classifier.

**Non-linear SVM:** Non-Linear SVM is used for non-linearly separated data, which means if a dataset cannot be classified by using a straight line, then such data is termed as non-linear data and classifier used is called as Non-linear SVM classifier.

## ↳ Hyperplane and Support Vectors in the SVM algorithm: 

**Hyperplane:** 

There can be multiple lines/decision boundaries to segregate the classes in n-dimensional space, but we need to find out the best decision boundary that helps to classify the data points. This best boundary is known as the hyperplane of SVM.

The dimensions of the hyperplane depend on the features present in the dataset, which means if there are 2 features (as shown in image), then hyperplane will be a straight line. And if there are 3 features, then hyperplane will be a 2-dimension plane.

We always create a hyperplane that has a maximum margin, which means the maximum distance between the data points.

**Support Vectors:**

The data points or vectors that are the closest to the hyperplane and which affect the position of the hyperplane are termed as Support Vector. Since these vectors support the hyperplane, hence called a Support vector.

## ↳ SVM Kernels

SVM kernel is a mathematical function that is used to map the data points from one space into another, usually higher dimensional space. When training a support vector machine (SVM) model using Sklearn SVC algorithm, the kernel hyperparameter can take on several values: **‘linear’, ‘poly’, ‘rbf’ and ‘sigmoid’.**

![SVM kernal formula](https://github.com/yagniksorathiya/SVM/assets/129974278/dc9fc8f4-5d77-4b5f-bf49-bf66bdced24d)

+ **When kernel is set to ‘linear’,** it means that the model will use a linear boundary for classification and regression. This is the simplest type of SVM and works best when data are linearly separable.

+ **When kernel is set to ‘poly’,** it means that the model will use polynomial functions of degree higher than 1 for classification. This type of SVM is more suitable for complex non-linear datasets.

+ **When kernel is set to ‘rbf’,** it means that the model will use radial basis funcitons for classification or regression. RBF kernels are capable of dealing with complex multi-class datasets and have good generalization performance with noisy data points.

+ **When kernel is set to ‘sigmoid’,** it means that the model will apply sigmoid functions instead of RBFs for classification or regression tasks. Sigmoid kernels tend to be less sensitive than RBFs with respect to outliers in data but may not generalize as well unless their parameters are tuned properly.

![sphx_glr_plot_iris_svc](https://github.com/yagniksorathiya/SVM/assets/129974278/9a83a86e-27e4-4c86-b703-1d3c07760441)

## ↳ How Does SVM Work?

As an example, let’s say we have a dataset with two features (x1 and x2) and two classes (0 and 1). We can visualize this data by plotting it in a two-dimensional space, with each point colored according to its class label. Look at the diagram below.

![support-vector-machine-which-hyperplane](https://github.com/yagniksorathiya/SVM/assets/129974278/146f59ed-b1ee-41c6-8533-e4dba9293fe3)

In the above case, we can see that there are different straight lines that can perfectly separate the two classes. However, we can still find a decision boundary that does a pretty good job. This boundary is generated by Support Vector Machine algorithm.  Using SVM algorithm, as mentioned above, training the model represents finding the hyperplane (dashed line in the picture below) which separates the data belonging to two different classes by **maximum or largest margin**. And, the points closest to this hyperplane are called **support vectors**. Note this in the diagram given below.

![support-vector-machine](https://github.com/yagniksorathiya/SVM/assets/129974278/5ccef657-6834-4ef1-b5dc-c0f6d14659de)

The blue square points represent one class and the red dots represent another class. The black line is the decision boundary learned by an SVM. As you can see, the SVM has placed the boundary in such a way as to maximize the margin between the two classes. Here is a visual representation of how SVM classification works. Note how original data set is projected into higher-dimensional space, then a decision boundary is found and finally the decision boundary is projected into original feature space.

![SVM-algorithm-visual-representation](https://github.com/yagniksorathiya/SVM/assets/129974278/512e195e-24f5-477a-a837-6743a3ff62d3)

Support vector machines are a powerful tool for classification, but like any machine learning algorithm, they require careful tuning of their **hyperparameters** in order to achieve optimal performance.

