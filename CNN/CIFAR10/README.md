# CIFAR-10 Image Classification Using a CNN

This project implements a Convolutional Neural Network (CNN) to classify images from the CIFAR-10 dataset, a standard dataset used in image recognition tasks. The model is built using PyTorch and is trained to classify images into 10 categories.

## Dataset

The CIFAR-10 dataset consists of 60,000 32x32 color images in 10 different classes, with 6,000 images per class:
- **Training Set**: 50,000 images
- **Test Set**: 10,000 images

Each image is labeled as one of the following:
1. Airplane
2. Automobile
3. Bird
4. Cat
5. Deer
6. Dog
7. Frog
8. Horse
9. Ship
10. Truck

## Features

- Implements a CNN with 3 convolutional layers and 2 fully connected layers.
- Includes ReLU activation functions, Batch Normalization, and MaxPooling for better performance.
- Applies Dropout for regularization.
- Uses Cross-Entropy Loss as the loss function and Adam optimizer for gradient descent.

## Model Architecture

The CNN consists of:
1. **3 Convolutional Layers**:
   - First Layer: 16 filters, kernel size = 3x3, stride = 1, padding = 1
   - Second Layer: 32 filters, kernel size = 3x3, stride = 1, padding = 1
   - Third Layer: 64 filters, kernel size = 3x3, stride = 1, padding = 1

2. **MaxPooling Layers**:
   - Reduces spatial dimensions by 50% after each convolutional layer.

3. **Fully Connected Layers**:
   - First Layer: 64x4x4 input units, 128 output units.
   - Second Layer: 128 input units, 10 output units (number of classes).

4. **Dropout**:
   - Dropout rate of 0.7 applied after the first fully connected layer.


## Training

- **Dataset Preprocessing**:
  - Images are normalized to have pixel values between 0 and 1.
  - Data is reshaped for input to the CNN.
  
- **Hyperparameters**:
  - Batch Size: 10
  - Epochs: 20
  - Learning Rate: 0.001

- **Optimizer**: Adam
- **Loss Function**: CrossEntropyLoss

## Acknowledgements
I thank [UCB CS189 Course](https://eecs189.org) for providing tutorials and homework that inspired and guided this project. I also thank [CIFAR-10 Dataset](https://www.cs.toronto.edu/~kriz/cifar.html) for the dataset.

