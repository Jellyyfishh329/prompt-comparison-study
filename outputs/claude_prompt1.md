# Claude: Prompt 1

_Pasted exactly as the tool returned it (image placeholders removed)._

---

A neural network is a function that learns to map inputs to outputs by adjusting a large number of numeric settings, called weights, until its predictions are good.

**The basic unit: a neuron**

Each artificial neuron does something simple. It takes several numbers as input, multiplies each by a weight (how much that input matters), adds them up with a bias (a baseline offset), and passes the result through an activation function. That function, such as ReLU (which zeroes out negatives) or sigmoid (which squashes values between 0 and 1), adds non-linearity. Without it, stacking layers would collapse into one big linear equation, and the network couldn’t learn anything complicated.

**Layers**

Neurons are arranged in layers. The input layer holds your raw data (pixel values, word embeddings, sensor readings). One or more hidden layers transform it step by step. The output layer produces the answer, such as a class probability or a predicted number. Each layer’s outputs become the next layer’s inputs. Early layers tend to pick up simple patterns (edges in an image), and later layers combine them into richer ones (eyes, then faces).

**Making a prediction (forward pass)**

Data flows through the layers: multiply by weights, add biases, apply activations, repeat. At the end you get a prediction. With random initial weights, that prediction is garbage.

**Learning**

Training is a loop:

1.  **Measure the error.** A loss function compares the prediction with the true answer and produces a single number: how wrong the network was.

2.  **Find who’s responsible.** Backpropagation uses calculus (the chain rule) to compute how much each weight contributed to the error, working backward from the output to the input. This gives a gradient for every weight.

3.  **Nudge the weights.** Gradient descent moves each weight a small step in the direction that reduces the loss. The step size is the learning rate.

4.  **Repeat** over many examples, usually in small batches, for many passes through the data.

Over thousands or millions of these updates, the weights settle into values that capture real patterns in the data.

**A useful analogy**

Imagine standing on a foggy hillside, trying to reach the lowest valley. You can’t see the whole landscape, but you can feel which direction slopes downward under your feet. You take a small step that way, check again, and repeat. The hillside is the loss, your position is the set of weights, and the slope is the gradient.

**Why it works**

With enough neurons and layers, a network can approximate almost any function. The real power is that you don’t hand-code the rules. You supply examples, and the network discovers useful internal features itself.

**Common pitfalls**

- **Overfitting:** the network memorizes the training data instead of generalizing. Fixes include more data, dropout, regularization, and early stopping.

- **Data hunger:** large networks need a lot of data and compute.

- **Opacity:** it’s hard to say exactly why a network made a given decision.

**Variants you’ll hear about**

Convolutional networks (CNNs) are specialized for images, recurrent networks (RNNs) for sequences, and transformers, which use attention to relate every part of the input to every other part, power modern language models like me.

If you’d like, I can walk through a tiny numeric example by hand, show a diagram, or write a small network from scratch in Python.
