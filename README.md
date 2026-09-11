# AlphaZero Connect Four:

An implementation of AlphaZero from scratch using PyTorch and Monte Carlo Tree Search.

The model learns Connect Four through self-play without using human game data.

## Design:

The fundamental principle behind Alphazero is a Monte carlo tree search that uses modified UCB values to guide search. 

During training, Alphazero will make predictions of the value and policy of a given state. MCTS then plays the game to completion. AlphaZero will then use the completed state from MCTS to determine a loss value and learn behavior

## Model Architecture:

The neural network used to train alphazero contains:
- A single Convolution layer that converts input into the correct shape (64 x 9 x 9)
- 128 Resnet blocks, each composing of 2 convolutions and 2 batchnorm layers
- A policyhead feed forward neural network that determines the polciy
- A valuehead feed forward neural network that determines the value

Input representation for the model:
- Channel 1: opponent pieces
- Channel 2: empty squares
- Channel 3: current player's pieces

## Results:
Results displayed using Kaggle Environments:

[![Watch AlphaZero gameplay](assets/gameplay-preview.png)](https://github.com/user-attachments/assets/66d1f823-bb2c-4a0c-bac9-c53a1ea5eaa1)

