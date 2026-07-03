# Neural Network From Scratch in NumPy — Backpropagation, Gradient Checking, L2, Dropout

A fully-connected deep neural network built entirely from scratch in NumPy — no PyTorch, no TensorFlow, no autograd. Every gradient is hand-derived using backpropagation and calculus, then numerically verified with gradient checking before being trusted for training. Trained and evaluated on MNIST.

**Keywords:** neural network from scratch, backpropagation from scratch, numpy deep learning, gradient checking, gradient descent, L2 regularization, dropout regularization, MNIST classifier, deep learning from first principles, machine learning fundamentals

## What makes this different from a typical "NN from scratch" tutorial

- **Hand-derived backpropagation** — full chain-rule walkthrough, including the combined softmax + cross-entropy Jacobian
- **Gradient checking** — every derived gradient is numerically verified against finite differences, so correctness is proven, not assumed
- **L2 regularization and Dropout**, implemented *and* mathematically derived — not just called from a library
- **Adaptive learning rate scheduling, early stopping, and checkpointing**, integrated into one training loop
- **A reusable, arbitrary-depth DNN class** — configure architecture, train, save/load parameters
- **Optional CuPy path** for GPU acceleration, as a drop-in NumPy replacement

## Why this exists

Most from-scratch neural network tutorials import NumPy, copy a formula, and call it done. This notebook takes the opposite approach: derive the math first, implement it second, and numerically prove the implementation matches the math before trusting a single training run. It's written to teach that method as much as the network itself — the goal is to be able to derive this yourself, not just run someone else's code.

If you've used Keras, PyTorch, or scikit-learn and want to understand what's actually happening under `.fit()` — this notebook is meant to take you from zero to "I could derive this myself," one step at a time, without skipping anything.

## What's covered

Building from first principles across 17 sections:
- The neuron and activation functions (sigmoid, ReLU, softmax)
- Math foundations — scalars, vectors, matrices, tensors
- Forward pass and network architecture design
- **Backpropagation**, derived by hand from the chain rule
- **Gradient checking** — finite-difference verification
- Mini-batch **gradient descent** (with a CuPy GPU-accelerated variant)
- Model checkpointing and early stopping
- Adaptive learning rate scheduling
- **L2 regularization** — derived and mathematically justified
- **Dropout regularization** — derived and mathematically justified
- A final, reusable, configurable DNN class trained on **MNIST**

## How to run

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]([<your-colab-link-here>](https://colab.research.google.com/github/Maitreya-Bhatkhande/neural-network-from-scratch-numpy/blob/main/nn_from_scrath.ipynb))

Or clone locally and open the notebook in Jupyter — requires only NumPy (and optionally CuPy for GPU acceleration).

## License

© 2026 Maitreya. All rights reserved. This notebook is shared publicly for learning and reference — feel free to read, learn from, and cite it with attribution, but please don't redistribute or repost it as your own.

If this helped you understand backpropagation or gradient checking better, a star on the repo is appreciated.
