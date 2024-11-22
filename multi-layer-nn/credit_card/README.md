# Credit Card Approval Prediction

This project implements a binary classification model to predict credit card approval using a dataset of applicant details. It uses PyTorch to build and train a multi-layer neural network.

## Dataset

The dataset contains anonymized information about credit card applicants. It includes both numeric and categorical features. Some columns have missing values (`?`) which are handled during preprocessing.

## Features

- Preprocessing:
  - Missing values in categorical columns are replaced with the most frequent value.
  - Missing values in numeric columns are replaced with the mean.
  - All categorical features are encoded into numeric values using `LabelEncoder`.
- Neural Network:
  - A multi-layer feedforward neural network is used for binary classification.
  - Binary Cross-Entropy Loss (`BCELoss`) is used as the loss function.
  - Stochastic Gradient Descent (SGD) is used as the optimizer.

## Model Architecture

The neural network architecture is as follows:
- Input Layer: Takes the feature vector as input.
- Two Hidden Layers:
  - Each with 256 neurons and ReLU activation.
- Output Layer:
  - Single neuron with Sigmoid activation for binary classification.

## Code Highlights

### Data Preprocessing
- Missing values (`?`) are handled:
  - For categorical columns: Replaced with the most frequent value.
  - For numeric columns: Replaced with the mean of the column.
- Features are standardized using `StandardScaler`.

### Training the Neural Network
- The model is trained using 600 epochs.
- A batch size of 10 is used with SGD as the optimizer and a learning rate of 0.15.
- Training loss is logged every 50 epochs.

### Evaluation
- Accuracy is computed for both training and testing datasets.
- Predictions are made by thresholding the output probabilities at 0.5.

## Results
- **Training Accuracy**: ~90% (varies depending on random seed and hyperparameters)
- **Testing Accuracy**: ~75% (varies depending on random seed and hyperparameters)

## Acknowledgements
- I thank Datacamp for providing the dataset and inspiration on this project. 
