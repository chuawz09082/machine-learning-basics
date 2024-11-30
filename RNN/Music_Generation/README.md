# Music Generation with RNNs

This project implements a Recurrent Neural Network (RNN) using PyTorch to generate music based on the dataset of songs. The model processes sequences of characters representing the songs and generates new sequences (songs) by sampling from the trained network.

## Features

- Utilizes **LSTM layers** to handle sequential data for song generation.
- Implements **character-level embedding** for vocabulary mapping.
- Generates new songs by sampling the trained RNN model.
- Includes integration with **Comet ML** for experiment tracking.
- Processes a dataset of songs, vectorizes them, and trains a character-level RNN.

## Model Architecture

The implemented RNN model consists of:

- **Embedding Layer**:
  - Maps character indices to dense vectors of a fixed size.
- **LSTM Layer**:
  - Processes the embedded sequences to learn sequential patterns.
- **Fully Connected Layer**:
  - Maps the LSTM's output to the vocabulary size for character prediction.

### Key Model Parameters:
- **Embedding Dimension**: 256
- **LSTM Units**: 1024
- **Batch Size**: 32
- **Sequence Length**: 100

## How It Works

### 1. Preprocessing
- The dataset of songs is loaded and joined into a single string.
- A vocabulary of unique characters is extracted.
- Characters are mapped to integers for training and reversed for text generation.

### 2. Training
- The RNN model is trained on sequences of characters using **CrossEntropyLoss**.
- The loss is minimized using the **Adam optimizer**.

### 3. Generation
- The model generates new songs by sampling one character at a time from the learned distribution, conditioned on previous characters.

## Dataset

The dataset is a collection of songs represented as strings. Each song is composed of characters, and the dataset is preprocessed to:
1. Join all songs into a single string.
2. Extract a **vocabulary** of unique characters.
3. Create mappings between characters and integer indices.

## Acknowledgements
I am grateful to Alexander Amini and Ava Amini for providing all the resources for [MIT 6.S191: Introduction to Deep Learning](https://introtodeeplearning.com).
