# Twitter Sentiment Analysis 

## ExpertsHub MLAI internship

==========================

## | Naive Bayes Classifier Model | 

### Introduction

Presenting an approach for classifying the sentiment of Twitter messages or tweets, these messages are classified as positive or negative with respect to a sentence. 

We have accomplished this by mining tweets using Twitter’s search API and subsequently processing them for analysis. Moreover, we use Distant Supervision, in which my training data consists of tweets with emoticons. 

Furthermore, we examine the effectiveness of three machine-learning techniques on providing a positive or negative sentiment on a tweet corpus. 

We test the effectiveness using Naive Bayes classifier, Maximum Entropy classifier, and Decision Tree classifier. We show that the accuracy of those algorithms is above 60% when trained with emoticon data.

In this internship, we have implemented two types of Naive Bayes classifier models using Python, Tweepy, and NLTK library. 

- Tweepy | There are excellent tutorials in its website http://www.tweepy.org 
- NLTK - Natural Language ToolKit | Please read the documentation found in its website http://www.nltk.org

In order to build a Twitter sentiment analyzer, first we need to understand the right tools and methods. Machine learning is one such tool where people have developed various methods to classify. Classifiers may or may not need training data. 

When training a classifier, supervised learning usually requires hand-labeled training data. With the large range of topics discussed on Twitter, it would be very difficult to manually collect and label enough data to train a sentiment classifier for tweets. 

One solution we propose is to use distant supervision, in which the training data consists of tweets with emoticons. The emoticons serve as noisy labels. 

For instance, :) in a tweet indicates that the tweet contains positive sentiment and :( indicates that the tweet contains negative sentiment. 

With the help of the Twitter API, it is easy to extract large amounts of tweets with emoticons in them. This is a significant improvement over the many hours it may otherwise take to hand-label training data.

### Implementation Details

- In order to work with this project, we used our Twitter developers account. 
- Later, we registered the client application with Twitter. 
- Created a new application and once we were verified we received the consumer token and secret for API Authentication.

CREATING THE DATASET

- We decided to create our own dataset based on emoticons such as ":)" and ":(" Then, we deleted them. Stripping out the emoticons causes the classifier to learn from the other features present in the tweet. The classifier uses these non-emoticon features to determine the sentiment.
- We have streamed thousands of tweets and stored them into a file
- Preprocess tweets
  * Lower case - we have converted the tweets to lower case 
  * URLs - We have eliminated all the URLs
  * #hashtag - hash tags can give us some useful information, so we have replaced them with the exact same word without the hash.
  * Punctuations and additional white spaces - we decided to remove punctuation at the starting and ending of the tweets.
- Feature Reduction (For example: Tokenization, Removing Stopwords, Twitter symbols, and Repeated Letters)


TRAINING THE CLASSIFIER 

- Naive Bayes is the classifier that we have used to create a sentiment analyzer. 
- The Naïve Bayes method in the NLTK library to train and classify.
- At this point, we have a training set, so all we need to do is instantiate a classifier and classify test tweets.

### Running the program
                                             
- First, save the three files (StreamingTwitter.py, StopWords.txt, and NaiveBayes.py) in the same folder.
- Second, execute the file StreamingTwitter.py, which will create your dataset.
- Third, execute NaiveBayes.py, which will run the classifier and ask you to enter a sentence (simulating a tweet)
- Finally, we will see if your sentence has a positive or negative feeling.
