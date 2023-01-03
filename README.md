# Forward-Forward implementation 

An implementation of Geoffrey Hinton's Forward-Forward (FF) algorithm in tensorflow.

## Introduction

In [this paper](https://www.cs.toronto.edu/~hinton/FFA13.pdf) Hinton proposed an alternative way to train neural networks, called Forward-Forward algorithm.

The main idea of the algorithm is that one can train the weights of each layer by comparing the results of a function called _goodness_ over two streams of outputs, _positive_ (we want the goodness to be above a threshold) and _negative_ (we want the goodness to be well below a threshold).

Here we propose an implementation of such algorithm in Tensorflow.

### Main points of the algorithm

The main points that made me curious to implement the algorithm are the following:

1. **Locality of training**. Each layer can be trained just comparing the outputs for a positive and a negative stream.
2. **Memory efficency**. Since we do not need to propagate activations back and forth, there is no need for storing activations.
3. **Immediate parameters update**. The algorithm does not have to wait the end of the forward pass and part of the backward one to update parameters, hence, there is an increase in trainig speed.

## Code implementation

Here we present a couple of notebooks, just for presentation examples.

### Future development

The aim is to collect here the code necessary to implement a package for training with forward-forward algorithm.

---

If you appreciate the project, show it by [leaving a star ⭐](https://github.com/oscar-defelice/tf-forward-forward/stargazers)
