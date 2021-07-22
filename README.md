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

## DATASETS

Bing Liu sentiment lexicon contains two .txt files for positive and negative words:
negative.txt  
positive.txt  
Restaurant review dataset taken from kaggle has also been submitted as ‘Restaurant_Reviews.tsv’

## RUNNING THE CODE

Set the sentence whose sentiment has to be found in the 2nd cell of ‘lexicon_based.ipynb’, 3rd cell of ‘without_discourse.ipynb’ and 5th cell of ‘with_discourse.ipynb’. ‘Run all’ to run the code.
The purpose of each cell in the submitted python notebooks has been summarised below:

### lexicon_based.ipynb:
1. Initialising the discourse relations and the respective attributes  
2. Initialising the test sentence whose sentiment has to be found. The sentence is tokenized using the nltk library  
3. Discourse function is implemented which takes a tokenized sentence as input and outputs the words(wij) and their respective discourse features(fij,flipij,hypij)  
4. Load the Bing Liu sentiment lexicon from the two text files  
5. Run the discourse function on the tokenized test sentence  
6. Using the sum product of features, the sentiment is calculated. Greater than zero signifies positive sentiment, equal to zero signifies neutral sentiment and less than zero    signifies negative sentiment.

### without_discourse.ipynb:
1. Importing python requirements  
2. Importing the restaurant review dataset  
3. Initialising the test sentence whose sentiment has to be found. The preprocessing of both the test sentence and dataset sentences is done  
4. Vectorizing the dataset using bag of words model imported from sklearn  
5. Splitting the dataset into train and test set  
6. Adding few manually labelled sentences containing the discourse relations because of unavailability of the discourse dataset  
7. Appending the manually labelled sentences and their labels to the training set  
8. Using SVM imported from sklearn for training the model.  
9. Vectorizing the test sentence using the same BoW model  
10. Predicting the sentiment and the probabilities from the trained SVM model  

### With_discourse.ipynb

1. Importing python requirements  
2. Initialising the discourse relations and the respective attributes  
3. Discourse function is implemented which takes a tokenized sentence as input and outputs the words(wij) and their respective discourse features(fij,flipij,hypij)  
4. Importing the restaurant review dataset  
5. Initialising the test sentence whose sentiment has to be found. The preprocessing of both the test sentence and dataset sentences is done  
6. Vectorizing the dataset using bag of words model imported from sklearn  
7. Appending the discourse features to the sentence vectors. Appropriate padding is done to ensure that vectors are of same dimensions  
8. Splitting the dataset into train and test set  
9. Adding few manually labelled sentences containing the discourse relations because of unavailability of the discourse dataset  
10. Appending the manually labelled sentences and their labels to the training set. These manually labelled sentences are also appended with the discourse features  
11. Using SVM imported from sklearn for training the model.  
12. Vectorizing the test sentence using the same BoW model. Adding the discourse features to the test sentences  
13. Predicting the sentiment and the probabilities from the trained SVM model  

## NOTES

The algorithm and implementation is directly inspired from :   
Mukherjee, Subhabrata & Bhattacharyya, Pushpak. (2013). Sentiment Analysis in Twitter with Lightweight Discourse Analysis. 24th International Conference on Computational Linguistics - Proceedings of COLING 2012: Technical Papers.







