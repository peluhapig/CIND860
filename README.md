# Capstone Project: Humor detection and ranking based on  Subreddit Data
## File Overview

ColBERT Data: https://github.com/Moradnejad/ColBERT-Using-BERT-Sentence-Embedding-for-Humor-Detection/tree/master/Data
Reddit Joke Data: https://github.com/taivop/joke-dataset

The models are included in the models folder.

The notebook included details of the developed model.

## Results Overview

Utilizing TinyBERT we achieved similar (only slightly worse) effectiveness to the ColBERT paper which used BERT using the ColBERT dataset with much better efficiency than compared to BERT. However, the dataset contains short jokes and newspaper titles, which have very different linguistic signatures, and therefore the model may not be training humor detection, but rather “what is a short joke and what is a newspaper” detection. That is a much easier problem than “Is this a joke”. Due to this, we switch to a dataset containing only Reddit jokes with a continuous score variabel that we then made binary by splitting the score at 10.  We saw that the model most likely considered the length of the joke as a key aspect in its prediction rather than the humor, and therefore we further considered two datasets, the total joke dataset and the long joke dataset. 
We saw that the model train on the long joke dataset was more effective with a precision of 0.723 and an accuracy of 0.531 as compared to the total joke model’s precision of  0.605 and an accuracy of 0.693. We saw that during the study of stability with different test sets our precision could even be around 0.75. However, most notably our median score of the uncurated long jokes is 9 and the median score of the curated jokes is 44. 
We have examined the efficiency of modern language models for humor detection and saw that TinyBERT achieved similar results to BERT, but still lacked some sophistication. We also see that indeed we can use language models to develop a tool for joke curation from raw unannotated data, as the median score increased to 44. 
