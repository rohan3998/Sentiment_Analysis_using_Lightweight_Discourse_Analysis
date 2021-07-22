# Sentiment_Analysis_using_Lightweight_Discourse_Analysis

We implement a method that will take into account several discourse relations
while predicting the sentiment of a sentence. Many sentiment analysis algo-
rithms record the polarity of the word however do not correctly capture the
context that leads them to make mistakes. We demonstrate how
connectives, conditionals and modals can be perceived as extremely valuable
context for sentiment prediction. We also highlight the different nuances of
dealing with different types of discourse relations. Using a lexicon based and
an SVM based approach, we showcase the advantage of using these discourse relations over a simple weighted polarity model.


The project uses three python codes shared in the form of notebook:

Lexicon_based.ipynb  : Implementation of lexicon based classification   
Without_discourse.ipynb : Implementation of sentiment analysis without using the discourse features  
With_discourse.ipynb : Implementation of sentiment analysis using the discourse features  

All the codes take sentence as input and output the sentiment of the sentence.

## INSTALLATION

numpy==1.18.5  
pandas==1.1.5  
nltk==3.2.5  
sklearn==0.22.2  
re==2.2.1  
python-csv

Pip install -r requirements.txt



