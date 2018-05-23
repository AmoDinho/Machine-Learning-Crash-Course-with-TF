# Regularization for Sparsity: L₁ Regularization

Creating feature crosses in a lot of dimensions increases the model size and will need lots of RAM to compute. We use L1 regularization to make the model weights zero. 

### L1 VS L2

Both penalize weights differently:
L2 penalizes weight^2
L1 penalizes the absolute value of weight

L1 AND L2 have different derivatives:
derivative of L2 is 2*weight
derivative of L1 is k

# Introduction to Neural Networks: Anatomy

**Hidden Layers**
In the model represented by the following graph, we've added a "hidden layer" of intermediary values. Each yellow node in the hidden layer is a weighted sum of the blue input node values. The output is a weighted sum of the yellow nodes.

**Activation Functions**

Sit behind a hidden layer as a nonlinear function and transforms the weighted sums. Common activation functions are Sigmoid and ReLU

What is a Neural Network:

- A set of nodes, analogous to neurons, organized in layers.
- A set of weights representing the connections between each neural network layer and the layer beneath it. The layer beneath may be another neural network layer, or some other kind of layer.
- A set of biases, one for each node.

- An activation function that transforms the output of each node in a layer. Different layers may have different activation functions.


One vs All -  there is a way to construct a NN that has multiple binary classifiers : For example, a model can tell between Fruit, Animals, Dogs 

# Multi-Class Neural Networks: Softmax

Softmax allows us to have multiple decimal probabilities for a multi-class problem. 

Full softmax vs candidate sampling - softmax calculates all the positive labels for a random sample of negative labels. 

If there are multiple classes then you need to use indivudal logistic regressions instead. 


# Embeddings: Motivation From Collaborative Filtering

collaborative filtering is about deteriming recommended samples of data based on previously consumed data that has similar charactistics. 

We can mapp data as embedings in multidimensional space. 

__Categorical Input Data__
these are input features that represent multiple discrete items from a finite set of
 choices.  

The problem with one-hot encoding a  NN with multiple classes is the size of the data and the large amount of computation required. So we need to turn large sparse vectors into a lower-dimensional space.

Principle Component Analysis is when you look for highly correlated dimensions that can be meged into a single dimension.


[Vector Representations of Words](https://www.tensorflow.org/tutorials/word2vec)
[Neural Networks, Manifolds, and Topology](http://colah.github.io/posts/2014-03-NN-Manifolds-Topology/)
