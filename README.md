# Financial Sentiment Analysis
## Problem 
Sentiment Analysis models have a variety of valuable uses such as monitoring social media posts to 
determine if any potential investment companies have negative news posted regarding themselves . 
Although, being able to scan through vast amounts of data and report findings is especially crucial in 
today’s environment however a lot of companies still do not use any type of machine learning models as 
these models have been proven difficult to deploy.

## Solution
The chosen solution to combat this problem is to build a Sentiment Analysis Model that can be deployed to 
quickly identity the emotional tone of a given text or article.

There are two main ways that a sentiment analysis model can be modelled on, Statistical or Neural 
Language Models. I choose to build my project model on a neural network model which makes use of Long 
Short Term Memory (LSTM) because it consistently outperforms statistical methods when predicting the 
outcome of a known text and neural networks exhibits better out of the box sample predictive accuracy 
than statistical models (Patricia M. West 387). The neural network will be trained on data set taken from the [Kaggle Website](https://www.kaggle.com/datasets/vivekrathi055/sentiment-analysis-on-financial-tweets) which has a total of 21995 unique values with a numeric sentiment values. 

## Project Pipeline

The project pipeline can be summarized in the following six steps:

- **Import and Illustration of the DataSet:** The first step in our process is to import the dataset and illustrate the data to help us better understand what we are dealing with.
- **Cleaning the Text from the DataSet:** In this step, we want to remove all tweets/text that do not have a sentiment value as well as ensure that there are no duplicates in our dataset. Then we can remove all stop words (words that do not add meaning to the sentence but are commonly used) and punctuation.
- **Tokenizing and Padding the Text:** Here, we are converting the text into a sequence of numbers and we then make use of padding to ensure each vector is of the same length.
- **Splitting Dataset:** Now we are getting close to building our model. This step is used to split our cleaned data into mulitple sets that can be used for training, validation and testing because how would we know if our model is even working if we don't test it?
- **Defining and Training the Model:** At this step, we are defining our model and its parameters as well as what type of layers we want to add to our neural network.
- **Using the Model to make Sentiment Predictions:** Once the model is done training, we can use a function that I defined to classify any tweets that spike our interest.
