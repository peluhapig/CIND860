# Capstone Project: Humor detection and ranking based on  Subreddit Data

Data Used: https://github.com/taivop/joke-dataset

The notebook included details of the developed model.

## Stage 1: Data 
First, we load and prepare the data, here we also decide on how we will be utilizing our score metric. We will be predicting if a Reddit joke had 0 reactions or some reactions. 
This decision was made due to the very skewed data and we will first give it an "easy" problem of simply saying if it's funny or not funny rather than a rating.
We also made a function that evenly splits our training and validation sets (80/20 split) to contain a balanced number of 1 and 0 score entries.

## Stage 2: Model Creation

We will be using Keras pre trained Bert model classifier, which does not require tokenized input, we see that the accuracy is mediocre reaching about 0.6691. Note that we used a sample size of 200 due to time constraints and runtime issues.

We then see our scatter plot, there is not much discernibility between the classification of 0's and 1's, and therefore the mediocre accuracy is misleading us to believe the model is more effective then it is.
