# MNIST Neural Network From Scratch 

## Why I Created This Notebook
I created this notebook for to learn about the basics of neural networks, driven by my interest in AI. The goal is to create a neural network from scratch which can classify handwritten digits. 

## Data
The dataset used for the training and evaluation can be found [here](/mnist_dataset/), it contains a small subsets of the MNIST data set, transformed into CSV format.

## Result
The [v4 notebook](/nn_from_scratch_v4.ipynb) achieved an accurary of 80%. This was achieved by using LeakyReLU instead of ReLU [[1](https://cs231n.github.io/neural-networks-1/#actfun)] [[2](https://pytorch.org/docs/stable/generated/torch.nn.LeakyReLU.html)] to fix the dying ReLU problem. 

| Network parameter    | Value     | Notes     |
|----------------------|-----------|-----------|
| Input layer          | 784 neurons |  |
| Hidden layer         | 200 neurons |  |
| Output layer         | 10 neurons  | Multi-class classification (10 numbers) |
| Hidden layer activation function  | LeakyReLU     |  |
| Final layer activation function | Softmax | Used for multi-class classification |
| Loss function        | Cross-entropy |  |
| Learning rate        | 0.00001      | This learning rate gives the least funky plot |
| Epochs               | 250         |  |
| Early stopping point | 92          | Check graph and log |
| Performance          | 0.8         |  |

## Observations 
Lowering the learning rate from 0.0001 to 0.00001 (10x), did not significantly increase the convergance point. This could be because of the use of LeakyReLU, which might offer faster convergance [[3](https://www.cs.toronto.edu/~fritz/absps/imagenet.pdf)]

## Links
[Kaggle](https://www.kaggle.com/code/konrads098/mnist-neural-network-from-scratch)