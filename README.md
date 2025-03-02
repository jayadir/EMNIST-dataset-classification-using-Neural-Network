# EMNIST Dataset Classification using Neural Network

## Overview
This project implements a feedforward neural network to classify characters from the EMNIST Balanced dataset. The model is built using TensorFlow and trained on a subset of EMNIST data.

## Dataset
The **EMNIST Balanced dataset** is used, containing images of handwritten characters. Each image is 28x28 pixels and belongs to one of 47 classes.

## Installation
To run this project, install the required dependencies:
```sh
pip install tensorflow tensorflow-datasets numpy matplotlib seaborn scikit-learn
```

## Running the Script
Run the script using:
```sh
python emnist_dataset_classification_using_neural_network.py
```

## Training the Model
The model is trained with different hyperparameters, including optimizer types, number of layers, and activation functions. Training can be modified within the script:
- **Number of hidden layers**: 3-4
- **Hidden layer sizes**: 64-512
- **Optimizers tested**: Adam, SGD, RMSprop, Momentum, Nesterov, Nadam
- **Epochs**: 10 (adjustable)
- **Loss function**: Sparse Categorical Cross-Entropy

## Accuracy Reports
Several configurations were tested, yielding different accuracies:
- **Best optimizer choices**: Adam, RMSprop, Nadam
- **Average accuracy**: ~80% on test data
- **Effect of loss function**: Cross-entropy performed significantly better than MSE
- **Effect of learning rate**: Higher rates reduced accuracy

### Accuracy Comparison of Optimizers
| Optimizer  | Test Accuracy (%) |
|------------|------------------|
| Adam       | 79.39            |
| SGD        | 6.15             |
| RMSprop    | 78.59            |
| Momentum   | 64.23            |
| Nesterov   | 62.71            |
| Nadam      | 79.43            |

## Visualization
The script plots:
- Training and validation accuracy
- Confusion matrix
- Accuracy comparison of different optimizers
- Loss comparison between Cross-Entropy and MSE

## Conclusion
For EMNIST classification, the best parameters include:
- **Adam, RMSprop, or Nadam optimizer**
- **Higher epochs** (e.g., 10+)
- **Cross-entropy loss function**

These configurations yield around **80% accuracy** on the test set.

