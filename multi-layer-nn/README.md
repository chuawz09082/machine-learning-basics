# FashionMNIST Classification with PyTorch

This project implements a simple multi-layer neural network using PyTorch to classify images from the FashionMNIST dataset. The model is trained on grayscale images of clothing items and evaluates its performance on unseen test data.

## Dataset
The [FashionMNIST](https://github.com/zalandoresearch/fashion-mnist) dataset contains:
- 10 categories of clothing items (e.g., T-shirt/top, trouser, dress, etc.).
- 28x28 grayscale images of clothing items.
- 60,000 training samples and 10,000 test samples.

## Project Overview
1. Data Preprocessing:
- The images are normalized to a range of 0 to 1.
- The data is split into training and testing datasets.
- `torchvision.transforms.ToTensor()` is used for preprocessing.

2. Model Architecture:
- A **fully connected feedforward neural network** with two hidden layers.
- **ReLU** activation function is used between layers.
- **CrossEntropyLoss** is used as the loss function.

3. Training:
- Stochastic Gradient Descent (SGD) optimizer is used.
- The model is trained for 50 epochs with a batch size of 10.

4. Evaluation:
- The model's accuracy is calculated on both the training and testing datasets.

## Acknowledgements
I thank [UCB CS189 Course](https://eecs189.org) for providing tutorials and homework that inspired and guided this project. I also thank [FashionMNIST Dataset](https://github.com/zalandoresearch/fashion-mnist) for the dataset.







