# MNIST Neural Network from Scratch

This is a neural network using just NumPy to understand the mathamatics under the hood. The network is trained on the MNIST dataset, which is a set of 28x28 pixel images of handwritten digits.

# How the Project Works

In this README, I'll walk you through the main steps of the code and what each part is doing.

# Data Loading and Preprocessing

We load the MNIST data. The dataset is publicly available on the internet. For this project I have pulled the dataset from kaggle. Each image is flattened into a vector so we can feed it into the neural network as input.
We split the dataset into two parts, training set and testing set.

# Network Architecture

The network itself is a simple fully connected feedforward neural network. I've kept it minimal: we've got an input layer, a hidden layer with a ReLU activation, and an output layer with a softmax activation. The ReLU activation helps introduce non-linearity, and the softmax at the end turns our outputs into probabilities for each digit class.

The images are 28 by 28 pixels where each pixel holds a value between 0 and 1 which represents the greyscale value of the corresponding pixel, ranging from 0 for black pixels to 1 for white pixels. This number inside the neuron is called its activation. 

We transpose the data so that each pixel can land one below each other vertically (visually only), as this makes it easier to perform matrix operation in them.

All these 784 pixels (28x28) form our first layer of the network. The last layer has 10 neurons each represent a one of the digits, the activation in these 10 neurons represents how much the system thinks that a given image corresponds with a given digit.

# Training Process

Training involves a basic forward pass to calculate predictions, and then a backward pass to update the weights using gradient descent.

Iteration represents number of times model updated its parameters. Alpha controls how aggressively the network updated its parameters.
To increase the accuracy I have trained the model with 1500 iterations and alpha value of 0.15.
both these settings are customizable easily in the code.

I've included comments in the code to explain how we calculate the loss, apply the gradients, and update the weights and biases step by step.

# Visualization

To make things a bit more visual, the code also uses Matplotlib to show the network’s predictions. That way, you can see how the model is doing as it learns.
To make a prediction, change the digit in test_prediction() function. Although the model is 92.83% accurate, it still lacks accuracy a lot. This is mainly due to the fact that this was just a simple project to understand how complex mathamatics like linerar algebra works under the hood of complex systems. Also the dataset is not enough to get better prediction and at last there is a lot of room for improvements that required heavy computation, data processing, opmization and large capital.
