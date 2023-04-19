# Seq2Seq_Transformer

## Overview

This is an implementation of a sequence-to-sequence model using the Transformer architecture in PyTorch. The model is designed to learn and predict patterns in numerical sequences. It uses custom Positional Encoding, Encoder-Decoder Transformer blocks, and target masking for effective training. The model has been tested and analyzed for its ability to learn and generalize different numerical patterns, showcasing its potential for various sequence-to-sequence tasks.


## Data Generation

The model was trained on synthetic input data containing various patterns and sequences of numbers, including zeros and ones, and other digits from 0 to 9. The input data was generated using the generate_random_data function, which created sequences of ones, zeros, and alternating ones and zeros of random length.

## Model Architecture

The Transformer model used in this implementation consists of the following layers:

- Positional Encoder: This layer adds positional information to the input embeddings, allowing the model to encode sequence information. The implementation includes a custom PositionalEncoding class that calculates and applies the positional encoding to the input sequence.

- Embedding: This layer maps the input tokens to a continuous vector space.

- Transformer Blocks: These are a stack of self-attention layers followed by feedforward layers. They allow the model to capture relationships between the input tokens and attend to different parts of the input sequence simultaneously.

- Output Layer: This layer maps the output of the Transformer blocks to the target vocabulary.

## Training

The model was trained using the Stochastic Gradient Descent (SGD) optimizer and CrossEntropyLoss loss function. The train_loop function was used to train the model for a specified number of epochs. The function includes a validation_loop to evaluate the model's performance on a validation set after each epoch. The model was trained for 10 epochs on the provided dataset. It uses custom Positional Encoding, Encoder-Decoder Transformer blocks, and target masking for effective training. 


## Evaluation

The model's ability to predict the next item in a sequence was evaluated by passing in a sequence of numbers and predicting the next item in the sequence using the predict function. The model was tested on several examples, including sequences of ones, zeros, and alternating ones and zeros. The predicted continuation of the sequences was compared to the actual continuation to evaluate the model's performance.
