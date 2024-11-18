# A Sentiment Analysis of the 2019 Australian Federal Election

On May 18, 2019, the 2019 Australian federal election was held to elect members of the 46th parliament of Australia. As is the case with many modern elections, many people around the world shared their thoughts and opinions regarding the election on Twitter, the popular social media site.

The purpose of this project is to perform a sentiment analysis on a large collection of tweets about the 2019 Australian election. We will analyze a dataset consisting of about 180,000 tweets, each of which has been assigned a sentiment label of "positive", "negative", or "neutral". We will construct a variety of machine learning classifiers, which we will use to predict the sentiment label of a given tweet based on the collection of words in the tweet.

In the end, we will compare the performances of our various models, and outline some possible applications of these models.


## The dataset

Our dataset consists of about 180,000 tweets about the Australian election, each of which has a sentiment label of "positive", "negative", or "neutral". The distribution of sentiments in these tweets is approximately 37% positive, 36% neutral, and 27% negative. For the purposes of training and testing our models, we reduce to a smaller dataset consisting of 10,000 such labelled tweets. 

## Preprocessing our data

Before passing our data to our models, we need to do some preprocessing. This includes the following steps.

- Remove all special characters
- Make all letters lower case
- Remove all "stopwords", which are words such as "the", "a", "to", etc., which have no bearing on the sentiment of a tweet.
- "Stem" each word. This means, for example, we replace any instance of the words "run", "running", "runner", etc. with a single representative word. This removes unnecessary complexity from out data.

After having cleaned our data, our next step is to "vectorize" our data. This means that we will convert each tweet into a vector, which is an input that we can feed into a variety of machine learning models. For this purpose, we use the "TfidVectorizer" from sklearn to convert each tweet into a vector of length 5000.

Finally, we split our data into a training set and testing set, and we are ready to build and train our models. 

## Building and training our models

We implement 5 different classification models of our sentiment analysis problem. Let's take a closer look at each one.

1. Naive Bayes Classifier
2. Decisino Tree Classifier
3. Random Forest Classifier
4. Logistic Regression
5. Support Vector Classifier (SVC)

We implement each of these models and train each on our training set. For several models, we also include a hyperparameter analysis to improve the performance of our model. More details can be found in the jupyter notebook. 

## Performance analysis and conclusions

After building, training, and testing each of our models, we find that the Support Vector Classifier (SVC) with rbf kernel is the most effective, achieving an accuracy of 79.7% on our testing set. 
