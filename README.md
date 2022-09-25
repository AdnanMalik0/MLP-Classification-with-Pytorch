# Multi-layer Perceptron Classification of MNIST dataset with Pytorch 

Classification of MNIST dataset using Multi-layer Perceptron (Neural Networks). The **"MAIN.ipynb"** file contains the implementation with brief explanation. The simple workflow includes:

1. Reading the image data (MNIST). Converting them into Pytorch tensors.
2. Creating a simple neural network based on Multi-layer Perceptrons. We use the torch.nn and torch.optim packages. These provide a simple way to build networks without losing sight of the iterative steps in gradient descent.

	First we construct the classifer function using the nn.Sequential wrapper that simply sequences the steps in the classifier function. In the case of a linear classifier there is just one nn.Linear layer. This is preceeded by nn.Flatten that vectorises a  28×28 input image into a 1D vector of length  28\*28

	Another experiment introduces a sigmoid activation layer (nn.Sigmoid). The activation layer allows transformation of input tensors such that complex intricate patterns from the input can be learnt.
3. We use Cross-Entropy loss when training our Deep network. Note, this takes log(Softmax) and Log-Likelihood, this means, it takes the probability of an input being equal to a certain output and gives loss based on this probability. This loss is further optimised to reduce by using Stochastic Gradient Descent as the optimiser.
4. Step-3 is repeated a number of times till the loss is reduced considerably.

A small comparison is also shown between the performace of 1-layer network and 2-layer network to give a good understanding of how the process works.




