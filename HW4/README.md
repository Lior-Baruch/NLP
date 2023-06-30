# Project Title: Deep Learning for Natural Language Understanding

This project focuses on the development and evaluation of deep learning models for natural language understanding tasks, specifically relation classification between two words in a sentence and sentence similarity prediction.

## Project Description

The aim of this project is to build and evaluate three different deep learning models that perform the following tasks:

1. **Relation Classification:** The first two models are designed to classify the relationship between two entities (words) within a given sentence. The models learn to discern the relationship context and categorize it into predefined classes. The classification is a multi-class problem where each class represents a specific type of relationship.

2. **Sentence Similarity Prediction:** The third model focuses on sentence similarity prediction. Given two sentences, the model computes a similarity score representing the degree of semantic similarity between them.

## Models

### Model 1: Fine-tuned BertForSequenceClassification

The first model is a fine-tuned `BertForSequenceClassification` model. `BertForSequenceClassification` is a BERT model with an added classification layer on top. In this project, the model is fine-tuned on a specific dataset for the relation classification task.

### Model 2: MTB

The second model, `MTB`, is a custom model that builds upon a base transformer model. It employs a strategy where all layers of the base model are frozen during training except for the classifier, pooler, and the 11th layer. The classifier is a linear layer that takes as input the concatenated representations of two entities (words) in the input sentence and outputs the classification logits.

### Model 3: SentenceTransformer

The third model is a `SentenceTransformer` model, specifically the `sentence-transformers/all-mpnet-base-v2` variant. This model generates embeddings for entire sentences, which are then compared using cosine similarity to predict the degree of similarity between two sentences.

## Setup and Dependencies

This project is implemented in Python and requires several packages including:

- numpy
- pandas
- torch
- transformers
- sentence_transformers

These can be installed via pip.

## Running the Project

To run the project, execute the provided Jupyter notebook. Ensure that all necessary Python packages are installed and the data files are placed in the correct directories.

## Results and Evaluation

The models' performances are evaluated using suitable metrics. For the relation classification task, precision, recall, and F1 score are computed. For the sentence similarity prediction task, the cosine similarity between sentence embeddings is used.

## Future Work

The models' performance can potentially be improved by fine-tuning the model architectures, training strategies, and hyperparameters. Additionally, the models can be evaluated on different datasets to assess their generalizability to different domains or contexts.
