# DVD Rental Prediction Project

This project aims to predict the number of days a customer rents a DVD based on various features like rental rate, amount paid, release year, and special features. The model uses a multi-layer neural network implemented in PyTorch, achieving an impressive Mean Squared Error (MSE) of less than 3 on the test set.


## Project Workflow

### 1. Data Preprocessing
- **Convert Dates**: Convert `rental_date` and `return_date` to datetime format and calculate the rental duration in days (`rental_length_days`).
- **Create Dummy Variables**: Generate dummy columns for special features like `Deleted Scenes` and `Trailers`.
- **Drop Unnecessary Columns**: Remove irrelevant features like `rental_date`, `return_date`, and `special_features`.
- **Standardize Data**: Normalize numerical features for efficient training using `StandardScaler`.

### 2. Model Design
The model is a **Multi-Layer Perceptron (MLP)** with:
- **Input Layer**: Matches the number of input features.
- **Two Hidden Layers**: Each with 256 neurons and ReLU activation.
- **Output Layer**: A single output neuron for predicting rental length.

### 3. Training
- **Loss Function**: Mean Squared Error (MSE) for regression tasks.
- **Optimizer**: Stochastic Gradient Descent (SGD).
- **Epochs**: 1000 iterations with a batch size of 10.

### 4. Evaluation
- Evaluate the model using the MSE metric on both training and test sets.

---

## Results

- **Training MSE**: ~1.35
- **Testing MSE**: ~1.89
