# Aspect-based Sentiment Analysis Algorithm based on Syntactic Parsing for Restaurant Review Dataset

## Introduction
A restaurant review is a type of evaluation of a restaurant. It can be brief or in-depth. Restaurant reviews are provided by people who have already dined in at a restaurant. Recognizing the sentiment of a restaurant review is a method of determining whether people liked or disliked a particular restaurant. Reviews help to provide some information about the ambience, service and food of a restaurant.

Classification of aspect terms in restaurant reviews as positive, negative or neutral is a part of Natural Language Processing (NLP). NLP helps computers read, understand and interpret human language. It is being widely used for sentiment analysis, language translation, text extraction, chatbots etc. Many different types of algorithms are used to perform text classification. With the increasing number of online platforms containing comments, reviews etc, the task of assigning a label to texts has high practical significance. It can be used to filter out toxic information or to simply understand the sentiment of text. Logistic Regression, Naive Bayes, Support Vector classifier etc. are some of the methods of performing text classification.

## Dataset 
The dataset used for this project is a restaurant review dataset. The dataset is a collection of reviews of restaurants. The training data is a xml file named “Restaurants_Train.xml'” and the testing data is “Restaurants_Test_Gold.xml”. Both files contain sentence id, text, aspect term, aspect term polarity, aspect category and aspect category polarity. The text contains the review text. The aspect term is the term for which the sentiment will be analysed. There are 3041 reviews in the training set and 800 the testing set. There are 2021 reviews containing at least one aspect term in the training set and similarly 606 in testing set. There are three possible values for polarity or sentiment of a term, namely, positive, negative and neutral. The distribution of classes is shown in Figure 1 and 2. Most of the polarity values are positive in both training and testing sets. This problem is a multi-class classification problem as there are more than two classes.

## Syntactic Dependency Parsing Method
The process of extracting a sentence's dependency parse to represent its grammatical structure is known as dependency parsing. Dependency parsing can be used to create an accurate dependency tree and tag each word with the appropriate dependency tag. A dependency tree is a directed graph in which one word is connected to another by an arrow pointing from the head word to the dependent words. Spacy library offers a fast and accurate dependency parser. The parser can also detect sentence boundaries and iterate over base noun phrases.

A system was designed which extracts the head.children and token.children for a given token. Here token refers to an aspect term in a review. It then combines all the words in the head.children and token.children to form a single text sentence. These two terms were combined to extract all the relevant information required to predict the sentiment for a token or aspect. The function getDictData() returns a dictionary with the combined text for all aspect terms as key and its polarity is the value of the key. The dictionary is then converted to a data frame with two columns, text and sentiment.

Further details about this project can be found in the Report_Sentiment Analysis.pdf .
