# Housing Prices Prediction

This project focuses on predicting housing prices using a dataset from the UCI Machine Learning Repository. The dataset contains various features related to housing characteristics and the median value of owner-occupied homes.

## Dataset
- **Source:** [UCI Machine Learning Repository](https://www.kaggle.com/datasets/heptapod/uci-ml-datasets)
- **File:** data.csv

### Column Descriptions
1. **CRIM:** Per capita crime rate by town
2. **ZN:** Proportion of residential land zoned for lots over 25,000 sq.ft.
3. **INDUS:** Proportion of non-retail business acres per town
4. **CHAS:** Charles River dummy variable (1 if tract bounds river; 0 otherwise)
5. **NOX:** Nitric oxides concentration (parts per 10 million)
6. **RM:** Average number of rooms per dwelling
7. **AGE:** Proportion of owner-occupied units built before 1940
8. **DIS:** Weighted distances to five Boston employment centers
9. **RAD:** Index of accessibility to radial highways
10. **TAX:** Full-value property-tax rate per $10,000
11. **PTRATIO:** Pupil-teacher ratio by town
12. **B:** 1000(Bk - 0.63)^2 where Bk is the proportion of blacks by town
13. **LSTAT:** % lower status of the population
14. **MEDV:** Median value of owner-occupied homes in $1000's

## Code Overview

1. **Importing Libraries:** Import necessary libraries such as NumPy, Pandas, Matplotlib, Seaborn.
2. **Loading the Dataset:** Read the dataset from the provided CSV file.
3. **Data Exploration:** Display the first three rows of the dataset and provide column descriptions.
4. **Data Cleaning:** Check for missing values and fill null values in the 'RM' column with the mean.
5. **Data Normalization:** Normalize the dataset using min-max normalization.
6. **Data Splitting:** Split the dataset into training and testing sets.
7. **Neural Network Model:** Build a neural network model using TensorFlow's Keras.
8. **Training the Model:** Train the model with 500 epochs, validate on a subset, and plot the loss.
9. **Model Fine-tuning:** Refine the model based on the loss vs. epochs plot and train for 100 epochs.
10. **Model Evaluation:** Evaluate the final model on the test set and calculate the Mean Squared Error (MSE).
11. **Prediction and Analysis:** Make predictions on the test set, compare with actual values, and calculate the total MSE on the test data.

## Usage
1. Ensure you have the required libraries installed (`numpy`, `pandas`, `matplotlib`, `seaborn`, `tensorflow`).
2. Download the dataset from the provided Kaggle link and save it as `data.csv` in the appropriate directory.
3. Run the provided Python script to execute the entire code.
4. Analyze the results, including the loss vs. epochs plot and the model's performance on the test set.

Feel free to experiment with the code, adjust hyperparameters, or explore additional features for better predictions.