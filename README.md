# MNIST digit recognizer Kaggle competition

In this notebook we will conduct analysis and modelling of MNIST dataset prepare for Kaggle [competition](https://www.kaggle.com/c/digit-recognizer).

MNIST ("Modified National Institute of Standards and Technology") is one of the most pupular datasets in machine learning world and handwritten images of digits. It served as the basis for benchmarking classification algorithms. To read more about MNIST dataset visit Yann LeCun's [website](http://yann.lecun.com/exdb/mnist/index.html).

## Framing the problem

In this competition our goal is to correctly identify digits from a MNIST dataset containing tens of thousands of handwritten images.We take an image of a handwritten single digit, and determine what that digit is. For every ImageId in the test set, we should predict the correct label.

The problem is clearly supervised learning problem: the data we have contains image representation along with it's true value label. This is also a classification task since we deal with discrete and finite number of categories that we want to assign to each of the input data. 

When it comes to performance measures for classification task like this one there are several options we could take. Kaggle competition defines the evaluation metric for this contest to be the categorization accuracy, meaning the proportion of test images that are correctly classified. We will follow this measure. Example categorization accuracy of 0.97 indicates that we have correctly classified all but 3% of the images.

Our submission file should be in the following format: For each of the 28000 images in the test set, output a single line containing the ImageId and the digit you predict. For example, if we predict that the first image is of a 3, the second image is of a 7, and the third image is of a 8, then our submission file would look like this:
```
ImageId,Label
1,3
2,7
3,8 
(27997 more lines)
```