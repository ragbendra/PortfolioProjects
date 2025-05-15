# Fake News Detection Project

This project uses machine learning to classify news articles as real or fake based on their text content.

## Requirements

- Python 3.x
- Pandas 1.2.4
- Scikit-learn 0.24.1
- NLTK 3.6.2

## Installation

Install the required libraries using pip:

```
pip install pandas scikit-learn nltk
```

## Dataset

The dataset used in this project is the "Fake and Real News Dataset" available on Kaggle: [https://www.kaggle.com/clmentbisaillon/fake-and-real-news-dataset](https://www.kaggle.com/clmentbisaillon/fake-and-real-news-dataset). Download the `True.csv` and `Fake.csv` files and place them in the `data/` directory.

Ensure that the paths in the code are set to `data/True.csv` and `data/Fake.csv`. If you place the files elsewhere, adjust the paths in the code accordingly.

## Usage

To run the project, execute the following command:

```
python fake_news_detection.py
```

## Model

The project employs the Multinomial Naive Bayes algorithm for classification and achieves an accuracy of 95% on the test dataset.