# Fake News Detection

### 4.1 Introduction

Our proposed system aims at reliably predicting and classifying the given piece of news as fake or true with the help of recurrent neural networks (RNNs) and long-short term memory (LSTM) algorithms. With the help of our proposed machine learning model, we lay a solid foundation for efficient detection of fake news by overcoming the limitations of the existing systems and trying to achieve higher accuracy rates.

To construct a machine learning model for fake news detection, we follow a step-by-step approach outlined in the modules below.

### 4.2 Understand The Problem And Business Case

In the current era of misinformation and fake news, the objective of this hands-on project is to identify fake news utilizing Recurrent Neural Networks (RNNs). Natural Language Processing (NLP) involves converting text into numerical representations, which are then used to train an AI/ML model for predictions. An AI/ML-based fake news detector is essential for companies and media to automatically assess the authenticity of circulating news. This case study involves analyzing thousands of news texts to determine their veracity.

### 4.3 Import Libraries And Datasets

This task entails importing necessary libraries from packages and acquiring both real and fake news datasets.

### 4.4 Perform Exploratory Data Analysis

This step involves adding a target class column to categorize news as real or fake. It includes concatenating real and fake datasets, combining Title and Text datasets, and exploring the combined dataset.

### 4.5 Performing Data Cleaning

Data cleaning is executed by removing stopwords (commonly used words with minimal meaning). A function is created to remove stopwords, considering a length criterion to enhance filtration. The task concludes by visualizing the data using a word cloud.

### 4.6 Visualising Cleaned Up Data

This task focuses on visualizing word frequency using word clouds. Additionally, the maximum length of words is determined for creating word embeddings.

### 4.7 Prepare the Data by Performing Tokenization and Padding

The data is divided into training and testing sets, and tokenization and padding are performed to prepare the data for LSTM network training.

### 4.8 Understand the Intuition behind Recurrent Neural Networks (RNN)

An overview of RNNs is provided, emphasizing their ability to work with sequences and address the vanishing gradient problem. Gradient descent as an optimization algorithm and the need for Long Short-Term Memory (LSTM) to overcome challenges are discussed.

### 4.9 Understand the Intuition between LSTM Networks

LSTM networks, a type of RNN, are introduced. The memory-holding capabilities of LSTMs, facilitated by gates regulating information flow, are explained with practical examples.

### 4.10 Build and Train the LSTM model

The LSTM model is constructed using an embedding layer for low-dimensional representation. Data is divided into training and testing sets, and the model is trained with a specified number of epochs.

### 4.11 Assess Trained LSTM Performance

The model's predictions are assessed using metrics such as accuracy_score and confusion_matrix to visualize classification results.

### 4.12 Summary

The process involves understanding the problem, importing libraries and datasets, performing exploratory data analysis, cleaning data, visualizing data, preparing data for LSTM, understanding RNN and LSTM intuition, building and training the LSTM model, and assessing its performance.
