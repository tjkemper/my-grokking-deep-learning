# Definitions



## Learning (in ML)
* Reducing error to 0

## Neural Networks (NN)
* Search for (and sometimes create) correlation between the input and output datasets. (p. 134 grokking deep learning)
* The sum total of the neurons, gradients, stacks of layers, and so on lead to a single idea: nerual networks find and create correlation.
* A series of weight matrices
* When you're using the network, you also end up creating vectors corresponding to each layer.
* NNs are like LEGO bricks, and each brick is a vector or a matrix

## NN Architecture
* The particular configuration of layers and weights in a neural network is called its architecture.
* Different architectures channel signal to make correlation easier to discover. (p. 138 grokking deep learning)
* Good neural architectures channel signal so that correlation is easy to discover.  Great architectures also filter noise to help prevent overfitting.

## Gradient Descent
* Make a prediction
* Calculate delta
* Adjust weights to bring error to 0

## Backpropagation
* Calculate deltas for intermediate layers so you can perform gradient descent
* What an earlier layer says it should be can be determined by teaking what a later layer says it should be and multiplying it by the weights in between them.  This way, later layers can tell earlier layers what kind of signal they need, to ultimately find correlation with the output.  This cross-communication is called backpropagation. (p. 135 grokking deep learning)
* When a neruon in the final layer says, "I need to be a little higher", it then proceeds to tell all the neurons in the layer immediately preceding it, "Hey, previous layer, send me a higher signal"
* It's like a giant game of telephone

## Vector-matrix multiplication
* Vector-matrix multiplication performs multiple weighted sums of a vector.  The matrix must have the same number of rows and the vector has values, so that each column in the matrix performs a unique weighted sum. (p. 139 grokking deep learning)

## Letters (p. 141 grokking deep learning)
* W0 => Weight matrix 0
* l0 => Layer 0
* l1 = relu(l0 W0)
* l2 = l1 W1
  * l2 = relu(l0 W0) W1
    * All the logic in the forward propagation step can be contained in this one formula

## Forward propagation
* Page 142 Grokking Deep Learning

## Regularization
  * The key to combatting overfitting in neural networks.
* A subset of methods used to encourage generalization in learned models, often by increasing the difficulty for a model to learn the fine-grained details of training data.
* Subset of methods to help the NN learn the signal and ignore the noise.
* Examples
  * Early stopping.  Use a validation set to know when to stop.
  * Dropout. Randomly turn off neurons (set them to 0) during training.
    * Dropout adds noise, making it more difficult for the network to train on the training data.

## Convolutional NN
* 

## Overfitting
* NN learned the noise in the dataset instead of making decisions based only on the true signal. (p. 150 Grokking Deep Learning)

## Batch gradient descent (p.158 grokking deep learning)
* CPU architectures are much faster at performing batched dot products.
* Taking the average of 100 noisy signals allows you to take bigger steps (larger alphas).
* Batch size: 8 to 256
* Generally, researchers pick numbers randomly until they find a batch_size/alpha pair that seems to work well.

## Activation functions
* Function applied to the neurons in a layer during prediction
* Constraints
  * Continuous and infinite
  * Monotonic (never change direction)
  * Nonlinear
  * Efficiently computable
* Standard hidden-layer activation functions (p. 165)
  * sigmoid [0, 1]
  * tanh [-1, 1]
* Output layer activation functions
  * Predicting raw values (no activation function)
  * Predicting unrelated yes/no probabilities (sigmoid)
  * Predicting which-one probabilities (softmax)
* Adding an activation to a layer changes how to compute delta for that layer.
  * If the node did not contribute to delta, do not update the weight
* 

## Parametric

## Nonparametric


