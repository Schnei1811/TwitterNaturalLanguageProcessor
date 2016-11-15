# TwitterNaturalLanguageProcessor
The Provided Scripts Run a Sentiment Analyzer of Incoming Tweets Using the Python Natural Language Took Kit. Of the Included Files:

TrainNLTK loads two 5000 line training sets (positive.txt and negative.txt) containing Twitter length positive and negative movie reviews. Initially, a pos and neg tag are appended to the end of each positive or negative string. Using the NLTK pos_tag function each sentence is tolkenized to distinguish parts of speech and if the part of speech is an adjective ("J") it is added to an all_word feature set. A frequency distribution of the collected adjectives is performed and words feature set refined to the 5000 most common adjectives. Two nested iterative functions then pass over each review to create the final dataset. Initially a dictionary is created for each review containing the 5000 most common adjectives and a boolean value of True if the adjective is found. Secondly, if the adjective was found to be true, it is categorized as either a positive or negative based on the tag previously given to the review. The end result is a dataset for each adjective entry of the 5000 most common adjectives found and a corresponding pos/neg classification. This featureset is then shuffled into a training and testing set (80% and 20% of the data respectively) and 5 classifiers (Naive Bayes, Multinomial Naive Bayes, Bernoulli Naive Bayes, Logistic Regression, and Linear Support Vector Classification) are trained on the data, report their accuracy (70-75%), and are saved as pickles. An example of the most informative features are listed below:

Most Informative Features
                    warm = True              pos : neg    =     17.6 : 1.0
                 routine = True              neg : pos    =     15.7 : 1.0
                 generic = True              neg : pos    =     14.4 : 1.0
                intimate = True              pos : neg    =     13.6 : 1.0
                    loud = True              neg : pos    =     13.0 : 1.0
                    flat = True              neg : pos    =     13.0 : 1.0
               inventive = True              pos : neg    =     13.0 : 1.0
                  boring = True              neg : pos    =     12.2 : 1.0
              refreshing = True              pos : neg    =     11.6 : 1.0
                 winning = True              pos : neg    =     11.6 : 1.0
                   urban = True              pos : neg    =     11.0 : 1.0
            heavy-handed = True              neg : pos    =     10.4 : 1.0
                haunting = True              pos : neg    =     10.3 : 1.0
                   vivid = True              pos : neg    =     10.3 : 1.0
               affecting = True              pos : neg    =     10.3 : 1.0

sentiment_mod loads a given string and classifies the string as a positive or negative message using the 5 saved pickles. Each vote is 

Graphs the Sentiment of Incoming Tweets Based on the Provided Key Word. 
