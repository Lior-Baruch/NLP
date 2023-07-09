# Named Entity Recognition (NER) with PyTorch

## Project Description

This project focuses on the task of Named Entity Recognition (NER), a subtask of information extraction that seeks to locate and classify named entities mentioned in unstructured text into pre-defined categories such as person names, organizations, locations, medical codes, time expressions, quantities, monetary values, percentages, etc.

We employ a bi-directional LSTM (Long Short-Term Memory) model, a type of Recurrent Neural Network (RNN), for this sequence labeling task. The project involves training the model with different configurations and evaluating its performance. Additionally, the project demonstrates how to utilize pretrained GloVe word embeddings in the models.

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Installation](#installation)
3. [Usage](#usage)
4. [Model Architecture](#model-architecture)
5. [Training](#training)
6. [Evaluation](#evaluation)
7. [Experimentation](#experimentation)
8. [Pretrained Embeddings](#pretrained-embeddings)
9. [Results](#results)

## Prerequisites

The project has the following dependencies:

- Python 3.7+
- PyTorch: A deep learning framework.
- NumPy: A package for scientific computing.
- pandas: A library providing high-performance, easy-to-use data structures and data analysis tools.
- sklearn: A machine learning library.
- seaborn: A data visualization library based on matplotlib.

## Installation

1. Clone this repository.
2. Install the required packages

## Usage

This project involves several steps, from data loading to model evaluation:

1. Load the data using the `load_data` function.
2. Preprocess the data using the `preprocess_data` function, which includes tokenization and lowercasing.
3. Create a vocabulary from the data using the `Vocab` class. This step converts words and tags into numerical IDs.
4. Convert the data into a format suitable for model training using the `Dataset` class. This step includes padding sequences for batch processing.
5. Instantiate the model using the `NERNet` class.

## Model Architecture

The `NERNet` class defines a bi-directional LSTM model for Named Entity Recognition (NER). The model includes:

1. An embedding layer that converts word IDs into word embeddings.
2. A bi-directional LSTM layer that takes word embeddings and outputs hidden states.
3. A linear layer that maps from hidden states to tag space.

## Training

The training loop is defined in the code, where the model parameters are updated for each batch. Loss is calculated using Cross Entropy Loss, and the Adam optimizer is used for optimization.

## Evaluation

The evaluation functions compute precision, recall, and F1-score for the model's performance on the validation and test datasets. A confusion matrix is also generated to give an overview of the model's performance.

## Experimentation

The project includes an experimentation section where various configurations of the model (varying hidden sizes, number of layers, and directions) are trained and evaluated. The results of these experiments are displayed in a table format.

## Pretrained Embeddings

This project also demonstrates how to incorporate pretrained word embeddings (specifically, GloVe embeddings) into the models. These embeddings are loaded into the model before training, and the impact on the model performance is evaluated.

## Results

After training and evaluation, the results are saved in CSV format. The results include precision, recall, and F1-score for each model configuration, both with and without 'O' tags.

## Conclusion

This project offers a comprehensive guide to implementing a Named Entity Recognition (NER) system using bi-directional LSTM in PyTorch, from preprocessing data to evaluating model performance. It also showcases the use of pretrained GloVe embeddings. The flexible design allows for easy experimentation with different model configurations and parameters.
