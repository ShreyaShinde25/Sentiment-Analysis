# Sentiment-Analysis
## Overview
This repository presents a custom deep learning model for sentiment analysis, focusing on classifying reviews as positive or negative. The project involves thorough data preprocessing, including cleaning and tokenization, followed by the design and training of a neural network. The primary goal is to achieve high accuracy in sentiment prediction, showcasing the integration of Natural Language Processing (NLP) methodologies and deep learning techniques.

## Data Preprocessing
The dataset **aclImdb** comprises 50,000 movie reviews evenly split between positive and negative sentiments. The preprocessing steps include loading training data, cleaning and preparing the text through lowercase conversion, tokenization, punctuation removal, stopword removal, and stemming. The processed data is combined into DataFrames for positive and negative reviews, then tokenized, padded, and split into training and testing sets.

## Network Design Choices
The neural network design incorporates key choices to enhance performance:

* **Embedding Layer:** Converts input text data into dense vectors of fixed size (128 in this case).
* **Convolutional Neural Network (CNN):** Utilizes Conv1D layer for feature extraction from embedded word vectors, suitable for sequential data like text.
* **Batch Normalization:** Stabilizes and accelerates the training process by introducing batch normalization after each convolutional layer.
* **Global Max Pooling Layer:** Reduces spatial dimensions, retaining crucial features.
* **Dropout Layer:** Mitigates overfitting and improves generalization.
* **Fully Connected Dense Layers:** Three layers optimized for better results.
* **Output Layer:** Sigmoid activation function for binary classification, producing probability scores between 0 and 1.

## Model Training and Testing
Training demonstrates improving loss and accuracy throughout epochs, with the model reaching a training accuracy of *98.29%*. Validation accuracy is approximately *86.44%*, achieved after around 10 epochs. The test accuracy is *85.62%*, consistent with the validation results, indicating the model's robust performance on unseen data.
