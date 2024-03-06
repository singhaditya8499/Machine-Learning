# COVID-19 NLP Text Classification

## Overview

This project focuses on sentiment analysis of COVID-19 related tweets using Natural Language Processing (NLP) techniques. The dataset used for this analysis is obtained from Kaggle, specifically from the [COVID-19 NLP Text Classification dataset](https://www.kaggle.com/datasets/datatattle/covid-19-nlp-text-classification).

## Table of Contents

1. [Introduction](#introduction)
2. [Project Structure](#project-structure)
3. [Data Cleaning and Preprocessing](#data-cleaning-and-preprocessing)
4. [Neural Network Models](#neural-network-models)
    - [Basic Neural Network](#basic-neural-network)
    - [Using the Embedding Layer](#using-the-embedding-layer)
    - [Recurrent Neural Network (RNN)](#recurrent-neural-network-rnn)
5. [Results](#results)
6. [Usage](#usage)
7. [Dependencies](#dependencies)
8. [Acknowledgments](#acknowledgments)
9. [License](#license)

## Introduction

The primary goal of this project is to analyze the sentiment of COVID-19 related tweets. The dataset used for this analysis is sourced from Kaggle and involves various preprocessing steps to clean the data. The sentiment analysis is performed using basic neural network models, models with embedding layers, and recurrent neural networks.

## Project Structure

The project is structured as follows:

- `data/`: Directory containing the dataset files. This is not included but can be downloaded to complete the pipeline.
    - `Corona_NLP_train.csv`: Original dataset file.
    - `cleaned_data.csv`: Cleaned and preprocessed dataset.
    - `super_cleaned_data.csv`: Further cleaned dataset used for model training.
- `src/`: Jupyter Notebooks containing the code.
    - `data_cleaning_and_EDA.ipynb`: Cleaning and preprocessing of the dataset.
    - `basic_nn_and_embeddings_and_RNN.ipynb`: Implementation of various neural network models.
- `README.md`: Detailed documentation.

## Data Cleaning and Preprocessing

The `data_cleaning_and_EDA.ipynb` notebook details the steps taken to clean and preprocess the dataset. Key steps include handling missing values, removing unnecessary columns, and applying text cleaning techniques to prepare the data for analysis.

## Neural Network Models

The `basic_nn_and_embeddings_and_RNN.ipynb` notebook focuses on building and training various neural network models for sentiment analysis. Three main types of models are implemented:

### Basic Neural Network

This model is a simple feedforward neural network trained on the preprocessed data.

### Using the Embedding Layer

A neural network model utilizing an embedding layer is implemented. This model aims to capture the semantic meaning of words and phrases.

### Recurrent Neural Network (RNN)

The RNN model incorporates bidirectional Long Short-Term Memory (LSTM) units for sequential data analysis. This model is designed to capture dependencies in the tweet text.

## Results

The training and evaluation results of each model are documented in the respective notebook sections. The accuracy is discussed.

### Basic Neural Network

Basic neural network model gave the accuracy of `43.17%` over the training dataset for 3 classes. For 5 classes, the accuracy was hovering around `29%`.

This model is not performing very well. It starts getting overfit when the network is expanded horizontally and underfits if the network is given the depth. I could'nt understand the issue in this.

### Using the Embedding Layer

The embedding model gave good accuracy when trained over a subset of 5000 training sample. Now we will run it for complete training data.

1. When the dimensions were set to 20, there was overfitting just after 6 epochs. The test accuracy achieved was `62%`. Possible reasons can be that the dimension space is too large.
2. With an embedding size of 50, we did prevented overfitting and stopped after 6 epochs (elbow noticed). The accuracy over test data is `64%`. We can further reduce the dimensions.
3. With an embedding dimension of 20, we achieved an accuracy of `65.16%` over the test data.
4. With an embedding dimension of 10, we achieved an accuracy of `64.91%` over the test data.
5. A strange phenomena, if we add 2 dense layers after the pooling layer the accuracy over the test data jumps to `67.63%`.
6. When adding 2 dense layers, first expanding the dimension (128) and then a 16 node layer, the accuracy over the test data is `68.75%`.
7. This is the best accuracy over the test data: `81.61%`. We had to reduce the number of classes from 5 to 3.

### Recurrent Neural Network (RNN)

1. When ran the RNN model over 3 classes for 5 epochs, the test data accuracy was `83.11%`. We are going with predefined learning rate, I think after 3 epochs we can reduce the learning rate and see the behaviour.
2. By expanind the RNN model both horizontally and verticall we were able to get an accuracy of `83.53%`. Not a significant improvement but decent enough. We will now try changing the Embedding dimensions.
3. By introducing 512 GRUs and with the same existing architecture, we can get an accuracy of `84.33%` over the training dataset.


## Usage

To reproduce the results, follow these steps:

1. Download the dataset from the [Kaggle dataset page](https://www.kaggle.com/datasets/datatattle/covid-19-nlp-text-classification) and place it in the `data/` directory.
2. Run the Jupyter notebooks in the `src/` directory in the specified order.

## Dependencies

Ensure you have the following dependencies installed:

- Python 3.x
- Jupyter Notebooks
- Libraries: pandas, numpy, matplotlib, seaborn, re, nltk, scikit-learn, keras, tensorflow

## Acknowledgments

- [Kaggle](https://www.kaggle.com/) for providing the COVID-19 NLP Text Classification dataset.

## License

This project is licensed under the MIT License