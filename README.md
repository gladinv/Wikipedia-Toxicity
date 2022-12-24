# Wikipedia-Toxicity

DESCRIPTION

Using NLP and machine learning, make a model to identify toxic comments from the Talk edit pages on Wikipedia. Help identify the words that make a comment toxic.

Problem Statement:  

Wikipedia is the world’s largest and most popular reference work on the internet with about 500 million unique visitors per month. It also has millions of contributors who can make edits to pages. The Talk edit pages, the key community interaction forum where the contributing community interacts or discusses or debates about the changes pertaining to a particular topic. 

Wikipedia continuously strives to help online discussion become more productive and respectful. You are a data scientist at Wikipedia who will help Wikipedia to build a predictive model that identifies toxic comments in the discussion and marks them for cleanup by using NLP and machine learning. Post that, help identify the top terms from the toxic comments. 

Domain: Internet

Analysis to be done: Build a text classification model using NLP and machine learning that detects toxic comments.

Content: 

id: identifier number of the comment

comment_text: the text in the comment

toxic: 0 (non-toxic) /1 (toxic)

Steps to perform:

Cleanup the text data, using TF-IDF convert to vector space representation, use Support Vector Machines to detect toxic comments. Finally, get the list of top 15 toxic terms from the comments identified by the model.

Tasks: 

Load the data using read_csv function from pandas package

Get the comments into a list, for easy text cleanup and manipulation

Cleanup: 

Using regular expressions, remove IP addresses

Using regular expressions, remove URLs

Normalize the casing

Tokenize using word_tokenize from NLTK

Remove stop words

Remove punctuation

Define a function to perform all these steps, you’ll use this later on the actual test set

Using a counter, find the top terms in the data. 

Can any of these be considered contextual stop words? 

Words like “Wikipedia”, “page”, “edit” are examples of contextual stop words

If yes, drop these from the data

Separate into train and test sets

Use train-test method to divide your data into 2 sets: train and test

Use a 70-30 split

Use TF-IDF values for the terms as feature to get into a vector space model

Import TF-IDF vectorizer from sklearn

Instantiate with a maximum of 4000 terms in your vocabulary

Fit and apply on the train set

Apply on the test set

Model building: Support Vector Machine

Instantiate SVC from sklearn with a linear kernel

Fit on the train data

Make predictions for the train and the test set

Model evaluation: Accuracy, recall, and f1_score

Report the accuracy on the train set

Report the recall on the train set:decent, high, low?

Get the f1_score on the train set

Looks like you need to adjust  the class imbalance, as the model seems to focus on the 0s

Adjust the appropriate parameter in the SVC module

Train again with the adjustment and evaluate

Train the model on the train set

Evaluate the predictions on the validation set: accuracy, recall, f1_score

Hyperparameter tuning

Import GridSearch and StratifiedKFold (because of class imbalance)

Provide the parameter grid to choose for ‘C’

Use a balanced class weight while instantiating the Support Vector Classifier

Find the parameters with the best recall in cross validation

Choose ‘recall’ as the metric for scoring

Choose stratified 5 fold cross validation scheme

Fit on the train set

What are the best parameters?

Predict and evaluate using the best estimator

Use best estimator from the grid search to make predictions on the test set

What is the recall on the test set for the toxic comments?

What is the f1_score?

What are the most prominent terms in the toxic comments?

Separate the comments from the test set that the model identified as toxic

Make one large list of the terms

Get the top 15 terms
