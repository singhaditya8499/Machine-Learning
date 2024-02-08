# Fashion MNIST Classification

This repository contains a Python script for training and evaluating a neural network model on the Fashion MNIST dataset using TensorFlow and Keras. The Fashion MNIST dataset is a collection of grayscale images of clothing items, each belonging to one of the ten different classes.

## Dataset

The dataset used in this project is the Fashion MNIST dataset, which consists of two CSV files: `fashion-mnist_train.csv` for training data and `fashion-mnist_test.csv` for testing data. The training data contains 60,000 samples, and the testing data contains 10,000 samples. Each sample is a 28x28 grayscale image of a clothing item, and the corresponding label represents the class of the item.

## Requirements

Make sure you have the required dependencies installed before running the script. You can install them using:

```bash
pip install pandas numpy tensorflow matplotlib seaborn
```

## Usage

1. Clone the repository:

```bash
git clone https://github.com/your-username/fashion-mnist-classification.git
```

2. Navigate to the project directory:

```bash
cd fashion-mnist-classification
```

3. Run the script:

```bash
python fashion_mnist_classification.py
```

The script will load the dataset, preprocess the data, build a neural network model, train the model, and evaluate its performance. It will also generate plots showing the training and validation loss, as well as training and validation accuracy over epochs.

## Results

The script uses a neural network with a specific architecture:

- Input Layer: Flatten layer for flattening the 28x28 images.
- Hidden Layer 1: Dense layer with 512 units and ReLU activation.
- Hidden Layer 2: Dense layer with 128 units and ReLU activation.
- Output Layer: Dense layer with 10 units and Softmax activation.

The model is compiled using the Adam optimizer and sparse categorical crossentropy loss. After training for 100 epochs, the script evaluates the model on the test data and plots the training/validation loss and accuracy.

## Conclusion

Based on the initial analysis, it is observed that the optimal number of epochs for training is around 10. Therefore, the script fine-tunes the model with this information and re-trains it for 10 epochs. The final evaluation on the test data provides the model's accuracy.

Feel free to explore and modify the script for further experimentation or improvement.