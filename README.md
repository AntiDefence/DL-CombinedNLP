# DL-CombinedNLP

Introduction:
Welcome to the repository containing the code for text classification using different neural network architectures. This repository demonstrates how to preprocess text data, build and train neural network models, and visualize the training accuracy of each architecture. The goal is to classify text as either related to cost (label 1) or not (label 0).

Code Explanation:

Data Loading and Undersampling:

The code begins by importing necessary libraries and loading the dataset from a CSV file using pd.read_csv.
To address potential class imbalance, undersampling is performed to balance the number of samples with label 0 and label 1. Random indices from label 0 are sampled to create a new dataset.
The resulting DataFrame is shuffled.

Text Preprocessing:

Punctuation is removed from the text using the remove_punct function.
Stopwords are removed from the text using the remove_stopwords function.
The dataset is transformed, and a counter is created to count unique words.

Data Splitting and Tokenization:

The dataset is split into training and validation sets.
Text data is tokenized using the Tokenizer from Keras.

Padding Sequences:

Sequences are padded to have the same length using pad_sequences from Keras.

Model Creation and Training:

Several neural network architectures are created and trained, including LSTM, Bidirectional LSTM (Bi-LSTM), CNN, and SimpleRNN.
A function create_train_model is defined to compile, train, and return the history of each model.

Training Accuracy Visualization:

A subplot figure with a 2x2 grid is created to visualize the training accuracy of each architecture.
Training accuracy and validation accuracy over epochs are plotted for each model.

Instructions:

Make sure you have the necessary libraries installed (pandas, tensorflow, numpy, matplotlib, nltk).
Replace "YOUR CODE LOCATION.CSV" with the actual path to your CSV file containing the dataset.
Run the code in your preferred Python environment.
The code will preprocess the text data, build and train the neural network models, and display training accuracy plots for each architecture.
