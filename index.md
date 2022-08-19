---
layout: home
author_profile: false
---
Utilizing Twitter to Inform Stock Decision Making via Sentiment Analysis.

We are a group of Ben Tamo, Ignacio Bartol, Diego Fratta, Andrew Kim, and Luis Pimentel.
## Abstract

In the past, a lot of research from several different sources would have to be used to successfully try to accurately predict market trends and market events. In the modern era, social media has become a tool that can be utilized to capture public sentiment towards the market. This information can thus be utilize to predict market sentiment, and thus market movements. This project attempts to tap into the data that can be received from one social media, Twitter, and look if it is possible to predict market movements accurately.

## Project Summary

The main goal of the project was to use machine learning to predict stock price movement solely based on popular tweets during that day. The project focuses particularly on the stock price of Tesla or `$TSLA$`.

#### Background

Prediction models for stock price fluctuations have always been a topic of interest. Being able to predict these changes can lead to financial gain. In the past, prediction was often done by consulting multiple sources in order to get an accurate prediction, known as stock fundamental analysis. Recently, there has been growing interest in the influence of social media over the stock market. In the case of this project, we studied Twitter to predict stock movement. The model is split into two parts to first classify the language of tweets then create predictions based on that classification. For the considered scope we did not have other technical parameters (such as the volume traded,hourly variations, etc.) influence our predictions, since the final objective is to asses only the effect of public opinion in one particular stock.

#### Data Collection

The project includes two datasets: a dataset of tweets and a separate dataset of stock price movements. Relevant tweets were scraped with the keywords “TSLA”, “delay”, “bull” and “bear”. These tweets were then manually labeled with their sentiment in order to fine-tune the sentiment classifier. The tweets were used for training, validation, and testing. Stock data was then collected using the records from the NASDAQ. In particular, the opening and closing prices were taken to determine if the stock price increased or decreased that day to be used as labels.

#### Methodology

The sentiment classification model is a pretrained language transformer called “DIstillBERT”. The model splits words and symbols in the text and outputs an embedding based on the vocabulary. The embedding is then put through the language encoder and a classification layer is trained to classify sentiment. 

The prediction model explored three different ML methods: a two layer dense neural network with three different preprocessing/regularization steps, an SVM, and logistic regression. The parameters input were the Sentiment Analysis of the tweets, the volume of tweets, and the tweet score for a specific day. The result of the model predicts price direction of a stock for that day.

#### Accomplishments

In the end, we trained the pipeline developed for classification and prediction with the dataset. Unfortunately, we had found a large case of overfitting, but the model was fairly accurate. There were serious limitations to the dataset as most tweets were classified as neutral, with a low amount of positive and negative tweets. This made it difficult for the Sentiment Analysis model to accurately train and thus having good classification results.

## Detailed Description 

#### Introduction 

Using machine learning techniques to predict stock prices is a widely researched topic. Works such as [1] explore using web query volume to predict stock prices. Trying to predict stock movement is not only an interesting topic, but successful models can lead to informing investors to make good financial decisions.
