# Disaster Tweet Analysis

## Table of Contents
  * [Overview](#overview)
  * [Motivation](#motivation)
  * [Approach](#approach)
  * [Technical Aspect](#technical-aspect)
  * [Installation](#installation)
  * [Run](#run)
  * [Bug / Feature Request](#bug---feature-request)
  * [Technology Stack](#technology-stack)
  * [Credits](#credits)


## Overview
Twitter has become an important communication channel in times of emergency. Thus, identifying genuine tweets regarding disaster has become even more important. Thus, through this project, an attempt has been made to identify if a tweet is about a real disaster or not. The problem is also a part of [Kaggle competition](https://www.kaggle.com/c/nlp-getting-started/overview).

## Motivation
False news have increased exponentially as the time has passed. And these news can sometimes might lead to dead end. Thus, if we can identify the difference between a tweet that is about a real disaster or not could be great start towards the end of this false news that are hovering around these days someday. A lot of attempt is being made nowadays to eradicate this problem, this what can be better than helping the world to be a better place even if it is by a bit.

## Approach
At first, data is cleaned by removing all the stopwords(and, a, the etc), applying contractions, applying lemmatization and stemming techniques so that the words like receiving and received will be transformed in its root form i.e receive. Also, the tweets are coverted into small letters so that words like Python and python would be treated as same word. Any non-alphabetical character is removed.

In order to classify the tweets, I tried with all the traditional machine learning algorithms. I tried using the feature extraction techniques like tfidf, word2vec and then gave those feature to the classification algorithms like logistic regression, or a basic one layer LSTM architecture, but those could not gave good results. Therefore, I went for BERT, by fine-tuning the weights in accordance with the given data. It gave better results. My submission in the Kaggle competition is rated under top 22%.

## Technical Aspect
BERT is being used to classify the tweet as disastrous or not. BERT being the state-of-the-art model to understand the context, could really prove out to be a handy tool. BERT is being fine-tuned over the dataset. Kaggle's [dataset](https://www.kaggle.com/c/nlp-getting-started/data) has been used for the project.

## Installation
Open a google colab notebook and run the cells.


## Bug / Feature Request
If you'd like to request a new feature/approach, feel free to do so by opening an issue [here](https://github.com/Shubhamm097/Disaster-Tweet-Analysis/issues/new). Please include the relevant reasons for the feature or approach.

## Technology Stack
1. PyTorch
2. Python
3. BERT Architecture
4. Keras


## Credits
- [BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding](https://arxiv.org/abs/1810.04805)

- [BERT repository](https://github.com/huggingface/transformers)

- [Fine-tune BERT for sentence classification](https://colab.research.google.com/github/DerwenAI/spaCy_tuTorial/blob/master/BERT_Fine_Tuning.ipynb)
