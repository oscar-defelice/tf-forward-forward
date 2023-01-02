# Forward-Forward implementation 

An implementation of Geoffrey Hinton's Forward-Forward (FF) algorithm in tensorflow.

## Introduction

In [this paper](https://www.cs.toronto.edu/~hinton/FFA13.pdf) Hinton proposed an alternative way to train neural networks, called Forward-Forward algorithm.

The main idea of the algorithm is that one can train the weights of each layer by comparing the results of a function called _goodness_ over two streams of outputs, _positive_ (we want the goodness to be above a threshold) and _negative_ (we want the goodness to be well below a threshold).

Here we propose an implementation of such algorithm in Tensorflow.
