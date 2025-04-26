# Sentiment Analysis using Python

## Overview
This project shows you how to use Python to figure out if tweets about airlines are positive or negative. It’s a fun way to learn how computers can understand feelings in text, using something called Sentiment Analysis.

## Purpose
The aim is to create a tool that can automatically tell if a tweet has a positive or negative vibe. This can help companies quickly see what customers think about them without reading every tweet by hand.

## Dataset
- We use a dataset with over 14,000 tweets, labeled as positive, negative, or neutral.
- For this project, we only care about positive and negative tweets, so we skip the neutral ones.
- You can grab the dataset from [this link](#) (add the real link if you have it).

## Tools and Libraries
Here’s what you’ll need to run this project:
- **Python 3.x**: The main programming language.
- **Pandas**: Helps us organize and work with the data.
- **Matplotlib**: Makes cool graphs to see our results.
- **TensorFlow**: Powers the machine learning part.

To install these, open your command line and type:
```bash
pip install pandas matplotlib tensorflow
```

## Steps to Build the Sentiment Analysis Model

### 1. Data Preprocessing
- **Load the Data**: We start by loading the tweets and picking just the text and sentiment (positive or negative).
- **Drop Neutral Tweets**: Since we’re only looking at positive and negative, we remove neutral tweets.
- **Turn Labels into Numbers**: Computers like numbers, so we change "positive" to 0 and "negative" to 1.
- **Prepare the Text**: We break the tweets into words (tokenization), give each word a number (encoding), and make all tweets the same length by adding zeros (padding).

### 2. Build the Text Classifier
- We use a special type of machine learning model called **LSTM** (Long Short Term Memory), which is great for understanding text.
- The model has:
  - **Embedding Layer**: Turns words into numbers that show their meaning.
  - **LSTM Layer**: Looks at the order of words to get the context.
  - **Dense Layer**: Decides if the tweet is positive or negative.
- We add **Dropout** to keep the model from memorizing the data too much, which helps it work better on new tweets.

### 3. Train the Model
- We use 80% of the tweets to teach the model and 20% to test how well it’s learning.
- We train it for 5 rounds (epochs) and check its progress.

### 4. Evaluate the Model
- After training, the model gets over 94% accuracy on the test tweets—pretty awesome!
- We make graphs with Matplotlib to see how its accuracy and errors change over time.

### 5. Test the Model
- We try it out with new sentences:
  - "I enjoyed my journey on this flight." → Predicts Positive
  - "This is the worst flight experience of my life!" → Predicts Negative

## How to Use the Code
1. **Get the Dataset**: Download it and put it in the right folder.
2. **Install the Libraries**: Use the command above to get everything set up.
3. **Run the Script**: Open the Python file and run it to process the data, build the model, train it, and test it.

## Summary
This project is a hands-on way to learn how Python and machine learning can figure out if text is positive or negative. It’s super useful for businesses to understand what people are saying about them online, like feedback about airlines.