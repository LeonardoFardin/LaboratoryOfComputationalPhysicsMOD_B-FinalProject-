# Laboratory of Computational Physics MOD B — Final Project

Final group project developed with G. Bregolin, L. Fogarolo, and F. Peron, awarded 30 cum laude.

## Overview

This project studies the **capacity of quantum neural networks (QNNs)** through the tools of Fisher information and effective dimension. It starts from the paper *"The power of quantum neural networks"* by Abbas et al., which argues that QNNs can be more expressive and more trainable than comparable classical networks.

We first **replicated** the main results of the paper, then **went beyond it** with additional analyses of our own.

## Replication of Abbas et al.

Following the paper, we compared a classical multi-layer perceptron with two quantum models (a QNN and an "easy" QNN, all with 4 features and 60 trainable parameters) on a binary classification task. We:

* computed the **Fisher information matrix** and its eigenvalue spectrum to check for barren plateaus;
* computed the **global effective dimension** as a function of the number of data samples;
* compared **training loss** and **test accuracy** across the models.

## Beyond the paper

* **PCA on the dataset**: reduction from 4 to 2 features, and its effect on performance and on the Fisher spectrum.
* **Number of qubits**: comparison of the Fisher spectra with 2 and 4 qubits.
* **Local vs global effective dimension**: the local version is computed around the trained weights, on both a synthetic and a binary dataset.
* **Single-neuron analysis**: the final neuron (classifier/regressor) is separated from the feature map, to understand whether a quantum neuron alone is more powerful than a classical one. This includes an analytical derivation of the Fisher information of both neurons, a regression task on a sinusoidal function, and a comparison with the VC-dimension bounds of Chen et al.
* **Role of entanglement**: effective dimension of QNNs with and without entanglement, compared with classical networks using different activation functions.
* **Quantum natural gradient**: a discussion of the metric in the quantum state space as a way to exploit its geometry during training.

## Repository structure

* `Giacomo_Bregolin_LCPB.ipynb`, `Leonardo_Fardin.ipynb`: notebooks with the analyses and simulations
* `FIM_Q/`, `Francesco/`, `Task_7/`: additional code and material for the individual parts of the project
* `Regression.pdf`: slides summarizing the project

## How to run

Install the required dependencies and run the notebooks using Jupyter.

## References

* A. Abbas, D. Sutter, C. Zoufal, A. Lucchi, A. Figalli, S. Woerner, *The power of quantum neural networks*, Nature Computational Science (2021).
* C.-C. Chen, M. Sogabe, K. Shiba, K. Sakamoto, T. Sogabe, *General Vapnik–Chervonenkis dimension bounds for quantum circuit learning*.
* *Effective dimension of machine learning models*.
