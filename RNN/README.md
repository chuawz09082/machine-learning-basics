# Vanilla RNN on FashionMNIST

This repository contains an implementation of a Vanilla RNN to classify the FashionMNIST dataset. Each image is treated as a sequence of rows, and the RNN processes the rows sequentially to classify the image into one of 10 categories.

## **Dataset**

The FashionMNIST dataset consists of grayscale images (28x28) of 10 classes:
- T-shirt/top
- Trouser
- Pullover
- Dress
- Coat
- Sandal
- Shirt
- Sneaker
- Bag
- Ankle boot

## **Model Architecture**

- **Input Layer**: Each row of the image (28 pixels) is treated as a time step in the RNN.
- **RNN Layer**: A single-layer Vanilla RNN with 40 hidden units processes the input sequence.
- **Output Layer**: A fully connected layer maps the RNN output to 10 classes.

## **Training**

- **Loss Function**: Cross-entropy loss.
- **Optimizer**: Adam optimizer.
- **Learning Rate**: 0.0005.
- **Epochs**: 500.

## **Results**

- **Final Training Accuracy**: 88.99%
- **Final Testing Accuracy**: 86.37%

## **Acknowledgements**
I thank [FashionMNIST Dataset](https://github.com/zalandoresearch/fashion-mnist) for the dataset. I am also grateful to Alexander Amini and Ava Amini for providing all the resources for [MIT 6.S191: Introduction to Deep Learning](https://introtodeeplearning.com).
