# Machine Learning Insurance Prediction

This repository contains two implementations of a machine learning model designed to predict whether a person will buy insurance based on their age and affordability. The dataset includes information on customers' age, affordability, and whether they bought insurance. This project demonstrates the basics of binary classification using both a neural network built from scratch and one using TensorFlow/Keras. Both models are trained and evaluated to explore different approaches to implementing machine learning algorithms.

## Project Structure
- **insurance_data.csv:** Dataset containing the features (age and affordability) and the target label (insurance purchased).
- **insurance_data-python.ipynb:** Jupyter notebook implementing a single-layer neural network from scratch using Python and NumPy. This implementation demonstrates a low-level approach to building neural networks and includes custom functions for forward and backward propagation, training, and evaluation.
- **insurance_data-tf.ipynb:** Jupyter notebook implementing a single-layer neural network using TensorFlow/Keras. This version leverages TensorFlow’s high-level API to build, train, and evaluate the model, showcasing a faster and more flexible approach to developing neural networks.
- **train_test_split:** Both implementations split the data into training and testing sets to evaluate the model's performance on unseen data.

## Key Components
### Custom Neural Network (insurance_data-python.ipynb)
- **Model Initialization:** Initializes weights and bias randomly and uses a sigmoid activation function for binary classification.
- **Training:** Implements forward and backward propagation manually to update weights and bias, using binary cross-entropy as the loss function.
- **Prediction and Evaluation:** Converts predicted probabilities to binary labels, calculates accuracy, and prints loss and accuracy metrics.
### TensorFlow/Keras Neural Network (insurance_data-tf.ipynb)
- **Model Definition:** Uses TensorFlow’s Sequential API to define a neural network with one dense layer and sigmoid activation.
- **Compilation and Training:** Compiles the model with the Adam optimizer and binary cross-entropy loss, and trains it with TensorFlow’s built-in methods for faster and more convenient training.
- **Prediction and Evaluation:** Evaluates the model using TensorFlow’s evaluate method, and uses a confusion matrix to visualize performance on the test set.

## Key Libraries
- **NumPy:** Used in the custom neural network implementation for matrix operations and numerical calculations.
- **TensorFlow/Keras:** Used in the high-level neural network implementation for efficient model building and training.
- **Pandas:** For data manipulation and preprocessing.
- **Seaborn and Matplotlib:** For plotting the confusion matrix and visualizing model performance.

## Acknowledgements
This project was inspired by the [Codebasics Machine Learning Tutorial on Neural Networks](https://www.youtube.com/watch?v=PQCE9ChuIDY&list=PLeo1K3hjS3uu7CxAacxVndI4bE_o3BDtO&index=13), which provided guidance on implementing neural networks and supplied the dataset used in this project. Special thanks to [Codebasics](https://www.youtube.com/@codebasics) for creating accessible and high-quality educational content on machine learning and data science.

