# Graph Neural Network (GNN) for Emotion Classification

Overview

This project implements a Graph Neural Network (GNN) for emotion detection from text using PyTorch and PyTorch Geometric. It leverages sentence embeddings generated by the SentenceTransformer model (all-MiniLM-L6-v2) and constructs a graph based on cosine similarity between sentence embeddings.

Dataset

The dataset comprises textual sentences labeled with specific emotions. It is split into:

Training data (train.txt)

Testing data (test.txt)

Features and Preprocessing

Sentence embeddings generated using the pre-trained SentenceTransformer model.

Labels encoded numerically using LabelEncoder.

Cosine similarity is computed to form graph edges; edges are created when similarity exceeds a specified threshold (default: 0.7).

Graph structured data is prepared for input into the GNN using PyTorch Geometric.

Model Architecture

Two-layer Graph Convolutional Network (GCN).

Fully connected layer for final emotion classification.

Activation function: ReLU.

Dropout for regularization (default rate: 0.5).

Training

Loss function: Negative Log-Likelihood (NLLLoss).

Optimizer: Adam with weight decay.

Training is conducted over multiple epochs (default: 100 epochs).

Evaluation

Evaluates model performance on a separate test dataset.

Metrics computed: accuracy, precision, recall, F1-score, and support for each emotion category.
