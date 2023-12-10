# NLP Deep Learning Project: Named Entity Recognition (NER)

## Overview

This project provides hands-on experience in building deep learning models for Named Entity Recognition (NER).

## Tasks

### Task 1: Bidirectional LSTM model

- **Objective**: Build a bidirectional LSTM model for NER.
- **Architecture**: Embedding → BiLSTM → Linear → ELU → Classifier
  - No flattening; the linear layer processes each hidden output of the BiLSTM layer.
- **Hyper-parameters**:
  | Layer | Hyperparam | Value |
  | -------------- | ----------------- | ----- |
  | Embedding | dim | 100 |
  | LSTM | Num LSTM layers | 1 |
  | | LSTM hidden dim | 256 |
  | | LSTM Dropout | 0.33 |
  | Linear | output dim | 128 |
- **Training**: Use any optimizer. Tune parameters like batch size, learning rate, and learning rate scheduling.

### Task 2: Using GloVe word embeddings

- **Objective**: Improve the BiLSTM model using GloVe word embeddings.
- **Implementation**:
  - Initialize neural network embeddings with GloVe vectors.
  - Freeze the embeddings.
  - Address the case-sensitivity conflict as GloVe is case-insensitive while NER model should be case-sensitive.

**Note**: The same solution may be used to enhance the score for Task 1.
