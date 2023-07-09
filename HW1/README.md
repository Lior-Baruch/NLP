# Language Model Creation and Testing from Tweet Data

## Overview

This repository contains a Jupyter notebook named `Assignment_1_LM_clean.ipynb`, developed as a part of an advanced course in Natural Language Processing (NLP). The objective of this assignment is to construct and evaluate language models, a fundamental component of NLP, using a dataset comprising tweets in multiple languages.

## Contents

The Jupyter notebook is divided into several sections, each corresponding to a unique stage in the process of language model creation and evaluation. 

### 1. Data Preparation

Before starting the assignment, data files should be prepared and stored under the directory `lm-languages-data-new`. These files include:

- English: `en.csv`
- Spanish: `es.csv`
- French: `fr.csv`
- Indonesian: `in.csv`
- Italian: `it.csv`
- Dutch: `nl.csv`
- Portuguese: `pt.csv`
- Tagalog: `tl.csv`
- A test dataset: `test.csv`

Each file contains tweets in the respective languages.

### 2. Preprocessing

This phase involves creating a unified vocabulary from all the data files. The function `preprocess` is implemented to iterate over each file and compile a list of unique tokens, where a token is defined as a single UTF-8 encoded character. This comprehensive list of tokens forms the vocabulary of our language model.

### 3. Language Model Creation

The heart of this assignment is the creation of a language model, which is accomplished using a function called `lm`. This function is designed to generate a language model from a provided textual corpus. In the context of this assignment, the corpus consists of the preprocessed tweets from different languages.

The language model constructed in this function is a type of n-gram model, a fundamental concept in Natural Language Processing (NLP). An n-gram is a contiguous sequence of n items from a given sample of text or speech, and n-gram models are used to predict the next item in such a sequence in the form of a (n-1)-gram.

The `lm` function creates a dictionary to represent the language model, with the following structure:

- **Keys:** The keys in the dictionary are all possible (n-1)-grams found in the corpus. For example, in a trigram model (n=3), if we have the sentence "I love dogs", the keys would be all the 2-grams: "I love", "love dogs". These (n-1)-grams are sequences of tokens that appear consecutively in the data.

- **Values:** The values in the dictionary are another dictionary that maps the nth token to its corresponding probability of occurrence after the specific (n-1)-gram. These probabilities are computed based on the frequency of the nth token following the (n-1)-gram in the training corpus.

For instance, let's consider a trigram model (where n=3), and we have the following entries in our dictionary:

```
{
  "I love": {"dogs": 0.8, "cats": 0.2},
  "love dogs": {"and": 0.5, ".": 0.5}
}
```

This implies that in the training corpus, after the sequence "I love", the word "dogs" appears 80% of the time and "cats" 20% of the time. Similarly, after the sequence "love dogs", half of the time it's followed by "and", and the other half it ends the sentence (represented by ".").

This dictionary-based representation of the language model serves as a probabilistic map, guiding the prediction of the next character based on the preceding sequence of characters.

It's important to note that the model incorporates a technique called add-one smoothing, which ensures that even unseen n-grams in the training data have a non-zero probability. This is critical for handling the diversity and variability of natural language data.

Through the `lm` function and the dictionary it generates, we create a statistical language model that can predict the next character in a sequence, providing a foundation for many NLP tasks such as text generation, auto-completion, and language identification.

### 4. Model Testing

The final part of the assignment involves evaluating the performance of the language model created. The model is tested on unseen data from `test.csv` to measure its effectiveness.

## Setup

To utilize this project:

1. Clone the course repository from GitHub: `https://github.com/kfirbar/nlp-course.git`
2. Install the required Python libraries, including numpy, pandas, and emoji.

## Usage

To execute the assignment:

1. Load the Jupyter notebook `Assignment_1_LM_clean.ipynb` in a Python environment (like JupyterLab, Jupyter Notebook, or Google Colab).
2. Run the cells in the notebook sequentially, starting from the top. The notebook provides step-by-step instructions through the process of data preprocessing, language model creation, and model testing.

## Output

The outputs of the assignment, including the created language models and their performance metrics, are saved to CSV files. This allows easy evaluation and further analysis. The notebook also provides console outputs to track the progress and results in real-time.

## Contributions

Since this is an academic assignment, contributions are not currently sought. However, the methods and code utilized in the assignment can serve as a foundation for other NLP tasks that involve language model creation and evaluation.

## License

This project is licensed under the terms of the MIT license. Please refer to the LICENSE file for more information.
