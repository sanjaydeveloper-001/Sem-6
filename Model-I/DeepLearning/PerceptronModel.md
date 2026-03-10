# Perceptron Model, Single Layer Perceptron and Multi Layer Perceptron

## 1. Perceptron Model

The **Perceptron** is one of the earliest and simplest types of artificial neural networks. It was introduced by **Frank Rosenblatt in 1957**. The perceptron is mainly used for **binary classification problems**, where the output belongs to one of two classes.

The perceptron mimics the working of a **biological neuron**. It receives several input signals, processes them, and produces a single output.

### Structure of a Perceptron

A perceptron consists of the following components:

1. **Input Layer**

   * The perceptron receives input values (x_1, x_2, x_3, ..., x_n).
   * These inputs represent features of the data.

2. **Weights**

   * Each input is associated with a weight (w_1, w_2, w_3, ..., w_n).
   * Weights represent the importance of each input.

3. **Bias**

   * Bias helps shift the decision boundary.
   * It allows the model to fit data more accurately.

4. **Summation Function**

   * The perceptron calculates the weighted sum of inputs.

[
z = \sum_{i=1}^{n} w_i x_i + b
]

5. **Activation Function**

   * The activation function decides whether the neuron should fire.
   * The most common function used in perceptron is the **step function**.

[
f(z) =
\begin{cases}
1 & \text{if } z \ge 0 \
0 & \text{if } z < 0
\end{cases}
]

### Working of Perceptron

1. Inputs are multiplied by their respective weights.
2. The weighted inputs are summed.
3. Bias is added to the sum.
4. The result is passed through an activation function.
5. The perceptron produces an output (0 or 1).

### Learning Rule

The perceptron learns by adjusting weights using the following rule:

[
w_{new} = w_{old} + \eta (target - output) x
]

Where:

* ( \eta ) = learning rate
* target = actual value
* output = predicted value

### Advantages

* Simple and easy to implement
* Efficient for linearly separable problems
* Requires less computational power

### Limitations

* Cannot solve **non-linear problems**
* Cannot handle complex patterns like XOR

---

# 2. Single Layer Perceptron (SLP)

A **Single Layer Perceptron** is the simplest type of neural network that contains **only one layer of neurons between input and output**.

It consists of:

* Input layer
* Output layer

There are **no hidden layers** in this model.

### Structure

Input nodes → Output neuron

Each input node connects directly to the output neuron with weights.

### Working

1. The input features are fed into the model.
2. Each input is multiplied by a weight.
3. The weighted inputs are summed together.
4. Bias is added to the sum.
5. The result passes through an activation function.
6. The final output is generated.

### Mathematical Representation

[
y = f\left(\sum_{i=1}^{n} w_i x_i + b \right)
]

Where:

* (x_i) = input
* (w_i) = weight
* (b) = bias
* (f) = activation function

### Example

Suppose we want to classify whether a student **passes or fails** based on study hours.

Inputs:

* Study hours
* Attendance

The perceptron combines these inputs using weights and produces an output:

* 1 → Pass
* 0 → Fail

### Advantages

* Easy to understand
* Fast computation
* Suitable for simple classification tasks

### Disadvantages

* Can only solve **linearly separable problems**
* Cannot solve problems like **XOR**

---

# 3. Multi Layer Perceptron (MLP)

A **Multi Layer Perceptron (MLP)** is an advanced neural network that contains **multiple layers of neurons**.

It is widely used in **machine learning and deep learning applications**.

### Structure of MLP

An MLP consists of three types of layers:

1. **Input Layer**
2. **Hidden Layer(s)**
3. **Output Layer**

Structure:

Input Layer → Hidden Layer(s) → Output Layer

### Hidden Layer

The hidden layer performs complex computations and feature transformations.
Multiple hidden layers allow the model to learn **non-linear relationships**.

### Activation Functions

MLP uses different activation functions such as:

* Sigmoid
* ReLU (Rectified Linear Unit)
* Tanh
* Softmax (for classification)

### Working of MLP

1. Input data is fed into the input layer.
2. Data is multiplied by weights and passed to hidden layers.
3. Each hidden layer performs transformations using activation functions.
4. The output layer generates the final prediction.
5. Errors are calculated using a loss function.
6. The network updates weights using **Backpropagation algorithm**.

### Backpropagation

Backpropagation is a training method used to minimize error by adjusting weights.

Steps:

1. Forward propagation
2. Calculate error
3. Propagate error backward
4. Update weights

### Advantages

* Can solve **non-linear problems**
* Handles complex datasets
* High prediction accuracy
* Used in deep learning models

### Applications

* Image recognition
* Speech recognition
* Medical diagnosis
* Fraud detection
* Natural language processing

### Limitations

* Requires more computation
* Needs large training data
* Training time is higher

---

# Conclusion

The **Perceptron model** is the basic building block of neural networks used for classification tasks.
The **Single Layer Perceptron** is simple and suitable for linearly separable problems but has limitations in solving complex patterns.
To overcome these limitations, the **Multi Layer Perceptron** was developed, which uses hidden layers and backpropagation to solve complex and non-linear problems, making it widely used in modern machine learning and artificial intelligence systems.
