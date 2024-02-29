# Auto MPG Prediction using Neural Networks

This Python script is designed to predict the Miles Per Gallon (MPG) of a car using a neural network. The dataset used in this script is sourced from [Kaggle](https://www.kaggle.com/datasets/uciml/autompg-dataset).

## Prerequisites

Before running the script, ensure you have the required Python libraries installed. You can install them using the following command:

```bash
pip install numpy pandas matplotlib seaborn tensorflow scikit-learn
```

## Usage

```python
python auto_mpg_prediction.py
```

## Overview

1. **Importing Libraries**: The necessary libraries are imported, including NumPy, Pandas, Matplotlib, Seaborn, and warnings. Warnings are suppressed for better readability.

2. **Loading the Dataset**: The script loads the Auto MPG dataset from the specified location.

3. **Peeking into the Dataset**: The first five rows of the dataset are displayed to provide a quick overview.

4. **Fetching Column Details**: The script provides information about the columns in the dataset, including a brief description of each.

5. **Handling Missing Values**: Checks for any missing or null values in the dataset and confirms that there are none.

6. **Data Types of Columns**: Displays the data types of each column and identifies an issue with the 'horsepower' column, which is resolved by replacing '?' values with the mean of the column.

7. **Descriptive Statistics**: Provides descriptive statistics for the numerical columns in the dataset.

8. **Handling 'Origin' Column**: Although 'origin' may not significantly impact the result, it is retained in the input features.

9. **Handling 'Car Name' Column**: The 'car name' column is dropped as it is not considered important for the prediction.

10. **Normalizing the Dataset**: Min-max normalization is applied to bring all features to a common scale.

11. **Splitting the Dataset**: The dataset is split into training and testing sets.

12. **Building the Neural Network**: A simple neural network is defined and compiled using TensorFlow's Keras API.

13. **Training the Model**: The model is trained on the training set with 300 epochs, and a plot of training and validation loss is displayed for analysis.

14. **Refining the Model**: The model is retrained with 100 epochs based on the observed loss pattern.

15. **Making Predictions**: The final model predicts MPG values on the test set.

16. **Evaluating the Model**: The script calculates the mean squared error loss on the test set.

## Notes

- The script uses a neural network with a specific architecture. You can customize the architecture by modifying the `getModel` function.

- The dataset used in this script is available on Kaggle, and the path to the dataset is specified in the script. Ensure you have the dataset or modify the path accordingly.

- The script provides a comprehensive overview of the data preprocessing, model training, and evaluation steps, making it suitable for understanding and extending for similar prediction tasks.