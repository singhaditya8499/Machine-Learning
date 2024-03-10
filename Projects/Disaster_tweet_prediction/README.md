# README

## Table of Contents
1. **Introduction**
2. **Data Cleaning**
   - `data_cleaning.ipynb`
3. **Basic Embedding-Based Model and Simple Neural Network**
   - `model_simple_tokenizer.ipynb`
4. **BERT for Text Classification**
   - `bert_torch_implmentation.ipynb`
5. **Instructions for Execution**
6. **Dependencies**
7. **Conclusion**

## 1. Introduction

This repository contains code files for text classification tasks, focusing on data cleaning, basic embedding-based models, and the implementation of BERT for text classification. The code is structured into three separate files, each serving a distinct purpose.

## 2. Data Cleaning

### Code File
- **File Name**: `data_cleaning.ipynb`

This code file focuses on cleaning the raw data for text classification. It performs the following tasks:
- Reads the raw data from a CSV file (`train.csv`).
- Drops unnecessary columns (`location` and `keyword`).
- Handles missing values in the `keyword` column.
- Cleans the text data by removing unwanted characters, expanding contractions, and performing other preprocessing steps.
- Saves the cleaned data to a new CSV file (`cleaned_data.csv`).

### Code File
- **File Name**: `model_simple_tokenizer.ipynb`

This code file builds a basic embedding-based model for text classification. It uses a simple neural network with dense layers for classification. The data is tokenized and padded, and the model is trained and evaluated on the training set.

## 4. BERT for Text Classification

### Code File
- **File Name**: `bert_torch_implmentation.ipynb`

This code file implements BERT for text classification using the Hugging Face `transformers` library. It includes the following key steps:
- Imports necessary libraries and loads the raw data.
- Defines a cleaning function (`clean`) for text preprocessing.
- Creates a custom dataset class (`TextClassification`) for BERT input format.
- Defines a BERT-based classification model (`BERTClassifier`).
- Splits the data into training and validation sets.
- Tokenizes and pads the text data using BERT tokenizer.
- Builds and trains the BERT model using PyTorch.
- Evaluates the model on the validation set.
- Applies the model to the test set and generates a submission file (`submission_bert.csv`).

## 5. Instructions for Execution

To run these code files, follow these steps:

1. Execute the first code file (`data_cleaning.ipynb`) to clean the raw data and save the cleaned data.
2. Run the second code file (`model_simple_tokenizer.ipynb`) to build and train a basic embedding-based model.
3. Execute the third code file (`bert_torch_implmentation.ipynb`) to implement BERT for text classification.

Note: Ensure that all required dependencies are installed before running the code files.

## 6. Dependencies

Ensure the following dependencies are installed:

- For Data Cleaning:
  - Python 3.x
  - pandas
  - numpy
  - matplotlib

- For Basic Embedding Model:
  - TensorFlow
  - scikit-learn

- For BERT Model:
  - PyTorch
  - transformers (Hugging Face)

## 7. Conclusion

This repository provides a comprehensive solution for text classification, covering data cleaning, basic embedding-based models, and BERT implementation. Feel free to customize the code to suit your specific needs. If you have any questions or issues, please reach out for assistance.

Happy coding!