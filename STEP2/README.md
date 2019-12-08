# This is STEP2

## Problem 1: Character recognition using a trained MLP

The purpose of this problem is to have you program, using numpy, the feedforward processing for
a multilayer perceptron (MLP) deep neural network.
The MNIST dataset of handwritten digits is widely used as a beginner dataset for benchmarking
machine learning classiers. It has 784 input features (pixel values in each image) and 10 output
classes representing numbers 0{9. We have trained a MLP on MNIST, with a 784-neuron input
layer, 2 hidden layers of 200 and 100 neurons, and a 10-neuron output layer. The activation
functions used are ReLU for the hidden layers and softmax for the output layer.
- (a) Extract the weights and biases of the trained network from mnist_network_params.hdf5.
The file has 6 keys corresponding to numpy arrays W1, b1, W2, b2, W3, b3. You may want
to check their dimensions by using the `shape' attribute of a numpy array.
- (b) The file mnist_testdata.hdf5 contains 10,000 images in the key `xdata' and their corre-
sponding labels in the key `ydata'. Extract these. Note that each image is 784-dimensional
and each label is one-hot 10-dimensional. So if the label for an image is [0; 0; 0; 1; 0; 0; 0; 0; 0; 0],
it means the image depicts a 3.
- (c) Write functions for calculating ReLU and softmax. These are given as:
![question1](../images/q1.png)
- (d) Using numpy, program a MLP that takes a 784-dimensional input image and calculates its
10-dimensional output. Use ReLU activation for the 2 hidden layers and softmax for the
output layer.
- (e) Compare the output with the true label from `ydata'. The input is correctly classied if the
position of the maximum element in the MLP output matches with the position of the 1 in
ydata. Find the total number of correctly classied images in the whole set of 10,000. You
should get 9790 correct.
- (f) Sample some cases with correct classification and some with incorrect classication. Visually
inspect them. For those that are incorrect, is the correct class obvious to you? You can use
matplotlib for visualization:
`import matplotlib.pyplot as plt`
`plt.imshow(xdata[i].reshape(28,28))`
`plt.show()`
Here, i is the index of the image you want to visualize, i.e. `xdata[i]` is a 784-dimensional numpy xarray.