
# Hyperparameter Tuning for Neural Networks with Keras Tuner

This project demonstrates the process of hyperparameter tuning for a neural network using Keras Tuner. The dataset used in this project is a synthetic moons dataset, which is commonly used for binary classification tasks.

## Project Overview

In this project, we:

1. **Import and preprocess the data:**
   - Load the moons dataset from a CSV file.
   - Split the data into training and testing sets.
   - Scale the features using `StandardScaler` for better model performance.

2. **Build a neural network model:**
   - Define a method `create_model` that allows Keras Tuner to tune various hyperparameters, including:
     - Activation function for hidden layers.
     - Number of neurons in the first layer.
     - Number of hidden layers and the number of neurons in each layer.
   - Compile the model using binary cross-entropy as the loss function and the Adam optimizer.

3. **Use Keras Tuner for hyperparameter tuning:**
   - Utilize the `Hyperband` tuner from Keras Tuner to search for the best hyperparameters.
   - The tuner searches over multiple epochs and configurations to find the best model.

4. **Evaluate the best model:**
   - The best model, as determined by Keras Tuner, is evaluated on the test dataset.
   - The final accuracy and loss are reported.

## Installation

To run this project, you need to have Python installed along with the required libraries. You can install the necessary dependencies using pip:

```bash
pip install keras-tuner pandas scikit-learn tensorflow
```

## How to Run the Project

1. **Install dependencies** as mentioned in the Installation section.
2. **Import necessary libraries** and load the dataset.
3. **Preprocess the data** by scaling the features using `StandardScaler`.
4. **Define the model creation function** `create_model` with hyperparameter options for Keras Tuner to search.
5. **Run Keras Tuner** to find the best model configuration.
6. **Evaluate the best model** using the test data and report the accuracy and loss.

## Results

- **Best Hyperparameters:**
  - Activation: 'relu'
  - First layer units: 9
  - Number of hidden layers: 2
  - Units in hidden layers: [5, 5, 5, 7, 7, 5]
  - Training epochs: 20

- **Model Evaluation:**
  - Accuracy: 93.60%
  - Loss: 0.1767

## Requirements

- Python 3.10
- Keras Tuner 1.4.7
- TensorFlow 3.3.3
- scikit-learn 1.0.2
- pandas 1.3.3

## Conclusion

This project showcases how to effectively use Keras Tuner for optimizing the hyperparameters of a neural network model. By tuning various aspects of the model, including the activation function and the number of layers/neurons, we were able to achieve a high accuracy on the test dataset.

## Acknowledgments

Special thanks to the Keras Tuner developers and the TensorFlow community for providing tools that make hyperparameter tuning accessible and effective.
