# Language Model Creation and Testing from Tweet Data

## Overview

This repository contains a Jupyter notebook named `Assignment_1_LM_clean.ipynb`, which is part of a series of assignments for an advanced course in Natural Language Processing (NLP). The goal of this assignment is to build and evaluate language models using a dataset that consists of tweets in multiple languages.

## Contents

The Jupyter notebook is divided into several parts, with each segment corresponding to a distinct phase in the process of language model creation and evaluation. Here are the key segments:

### Data Preparation

The assignment requires a set of tweet datasets in CSV format, each containing tweets in a different language. The datasets are:

- English: `en.csv`
- Spanish: `es.csv`
- French: `fr.csv`
- Indonesian: `in.csv`
- Italian: `it.csv`
- Dutch: `nl.csv`
- Portuguese: `pt.csv`
- Tagalog: `tl.csv`

In addition, there's a `test.csv` file for testing the model.

### Preprocessing

In this step, the data files are iterated over to create a unified vocabulary. The vocabulary comprises all unique tokens found in the data, with a token defined as a single UTF-8 encoded character.

### Language Model Creation

A function `lm` is implemented to generate a language model from the given textual corpus. The function returns a dictionary where the keys represent all relevant n-1 sequences, and the values are dictionaries with the nth tokens and their corresponding probabilities of occurrence.

### Model Testing

The final segment of the assignment involves testing the created language model on unseen data to evaluate its performance.

## Setup

To use this project:

1. Clone the course repository from GitHub: `https://github.com/kfirbar/nlp-course.git`
2. Install the necessary Python libraries, which include numpy, pandas, and emoji.

## Usage

To run the assignment:

1. Load the Jupyter notebook `Assignment_1_LM_clean.ipynb` in a Python environment (like JupyterLab, Jupyter Notebook, or Google Colab).
2. Execute the cells in the notebook in order, starting from the top. The notebook will guide you through the steps of the assignment, which include data preprocessing, language model creation, and model testing.

## Output

The results of the assignment, including the created language models and their performance metrics, are written to CSV files for easy grading and further examination. In addition to this, the notebook also provides output to the console to track the progress and results.

## Contributions

As this is an individual academic assignment, contributions are not currently sought. However, the techniques and code used in the assignment can be extended or modified for other related NLP tasks.

## License

This project is licensed under the terms of the MIT license. Please refer to the LICENSE file for more information.
