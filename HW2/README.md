# README

## Project Description

This project involves developing a part-of-speech (POS) tagger using a Hidden Markov Model (HMM). The dataset utilized in this project is sourced from the Universal Dependencies (UD) project. This Jupyter Notebook contains Python code for training, evaluating, and exporting results of the POS tagger. 

## Getting Started

### Dependencies

Ensure that the following Python packages are installed in your environment:

- os
- random
- nltk
- numpy
- pandas
- tabulate
- conllutils

You can install these dependencies using pip:

```bash
pip install os random nltk numpy pandas tabulate conllutils
```

### Instructions

1. **Dataset Analysis:** The first step involves loading the POS tagging dataset into a pandas DataFrame. Once loaded, perform exploratory data analysis to get insights about the dataset such as the total number of sentences, unique words, and unique tags.

2. **Data Preprocessing:** In this step, the raw data is transformed into a format that can be readily consumed by the machine learning model. This involves splitting the dataset into training and testing sets, and converting words and tags into numerical representations.

3. **Model Training:** Here, a Hidden Markov Model (HMM) is created and trained on the preprocessed training data. The goal of the model is to learn to predict POS tags for given sentences.

4. **Model Evaluation:** The trained model is then evaluated using the testing data. The performance of the model is quantified using the accuracy metric, which gives the proportion of tags correctly predicted by the model.

5. **Result Exportation:** The final step is to export the model's predictions on the testing data, along with the actual tags, to a CSV file. This allows for further analysis and comparison of the model's performance.

## Contributing

We welcome contributions to this project. Please follow the steps below to contribute:

1. **Fork** the repo on GitHub.
2. **Clone** the forked project to your local machine.
3. Make your changes and **commit** them to your local branch.
4. **Push** your changes to your forked repo on GitHub.
5. Create a **Pull request** so that we can review and merge your changes.

## License

This project is licensed under the terms of the license included in the repository. For more information, refer to the license file in the repository.

## Contact

For any queries or concerns related to this project, please feel free to contact the repository owner.
