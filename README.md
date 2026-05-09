# Neural Network From Scratch + Visual Playground

An interpretable neural network framework implemented from first principles using NumPy, featuring manual backpropagation, gradient verification, and visualization of learning dynamics.

---

# Features

- Fully connected neural network implemented from scratch
- Manual forward and backward propagation
- Binary cross entropy optimization
- Gradient descent training
- Interactive decision boundary visualization
- Streamlit-based experimentation playground
- Gradient checking for verification
- Experiments on optimization and representation learning

---

# Mathematical Foundation

## Forward Propagation

For layer \( l \):

$$
z^{(l)} = W^{(l)}a^{(l-1)} + b^{(l)}
$$

$$
a^{(l)} = \sigma(z^{(l)})
$$

where:
- **W⁽ˡ⁾** are learnable weights
- **b⁽ˡ⁾** are biases  
- **σ** is the activation function

---

## Binary Cross Entropy Loss

$$
L = -\frac{1}{n}\sum_{i=1}^{n}
\left[
y_i \log(\hat y_i)
+
(1-y_i)\log(1-\hat y_i)
\right]
$$

---

## Backpropagation

Using the chain rule:

$$
\delta^{(l)} =
\frac{\partial L}{\partial z^{(l)}}
$$

Weight gradients:

$$
\frac{\partial L}{\partial W^{(l)}} =
\delta^{(l)}(a^{(l-1)})^T
$$

Gradient descent update:

$$
W^{(l)} \leftarrow
W^{(l)} - \eta
\frac{\partial L}{\partial W^{(l)}}
$$

---

# Architecture

Current default architecture:

$$
2 \rightarrow 8 \rightarrow 8 \rightarrow 1
$$

Activation functions:
- ReLU
- Sigmoid
- Tanh

Optimizer:
- Gradient Descent

---

# Repository Structure

```text
nn/
visualization/
app/
experiments/
tests/
```

---

# Visualizations

## Decision Boundary Evolution

[PLACEHOLDER FOR GIF / SCREENSHOT]

---

## Loss Curve

[PLACEHOLDER]

---

## Hidden Layer Activations

[PLACEHOLDER]

---

# How To Run

## Clone Repository

```bash
git clone git@github.com:lusandamrasi/neural-network-playground.git
cd neural-network-playground
```

## Install Dependencies

```bash
pip install -r requirements.txt
```

## Run Streamlit App

```bash
streamlit run app/streamlit_app.py
```

---

# Experiments

- Logistic Regression vs Neural Networks
- Initialization studies
- Vanishing gradient analysis
- Activation function comparisons

---

# Future Improvements

- Adam optimizer
- Batch normalization
- Dropout regularization
- Multi-class classification
- CNN extension
- Real-time training animations

---

# Key Learning Outcomes

This project was built to deeply understand:
- matrix calculus
- computational graphs
- optimization
- gradient flow
- nonlinear representation learning
- neural network training dynamics