# Handwritten Digit Classification using Fully Connected and Convolutional Neural Networks

This project implements handwritten digit classification using the MNIST dataset. The models use PyTorch for training and evaluation, and Comet ML is integrated for experiment tracking.

## Features

- **Dataset**: MNIST handwritten digits dataset.
- **Preprocessing**: Data is normalized to range [0, 1].
- **Models**:
  - Fully Connected Neural Network (FCNN)
  - Convolutional Neural Network (CNN)
- **Visualization**: 
  - Display random samples from the training dataset.
  - Visualize predictions on the test dataset.
- **Experiment Tracking**: Uses Comet ML for logging training performance and visualizations.

## Dataset

- **Training Set**: 60,000 grayscale images (28x28 pixels).
- **Test Set**: 10,000 grayscale images.
- **Classes**: 10 (Digits 0-9).

## Model Architectures

### 1. Fully Connected Neural Network (FCNN)
- **Input**: Flattened 28x28 image (784 features).
- **Layers**:
  - Fully Connected Layer (784 → 128)
  - ReLU Activation
  - Fully Connected Layer (128 → 10)
- **Output**: 10 logits (one for each class).

### 2. Convolutional Neural Network (CNN)
- **Input**: 28x28 image with 1 channel.
- **Layers**:
  - Convolution Layer (3x3 kernel, 24 filters)
  - Batch Normalization
  - Max Pooling (2x2)
  - Convolution Layer (3x3 kernel, 36 filters)
  - Batch Normalization
  - Max Pooling (2x2)
  - Fully Connected Layer (900 → 128)
  - ReLU Activation
  - Fully Connected Layer (128 → 10)
- **Output**: 10 logits (one for each class).

## Results

### Fully Connected Network
- **Training Accuracy**: 100%
- **Testing Accuracy**: ~98%

### Convolutional Neural Network
- **Training Accuracy**: 100%
- **Testing Accuracy**: ~98%

## Acknowledgements
I grateful to Alexander Amini and Ava Amini for providing all the resources for [MIT 6.S191: Introduction to Deep Learning](https://introtodeeplearning.com).
