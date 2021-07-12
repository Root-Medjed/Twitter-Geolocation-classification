# Twitter-Geolocation-classification

In the past decades, the percentage of social media users grew rapidly. It has brought the attention that huge amount of information extracted from textual content on social medias such as Twitter can bring gigantic benefits to the society.

This project aims to explore the effectiveness of several Machine Learning models including Naive Bayes, Support Vector Machine and Logistic regression classifers among data set derived from the resource published by [Eisenstein et al., 2010], which is composed of three sets: train and develop-ment sets with labels which are used for training and evaluating the models; and the test set which is unseen and without labels used for the final evaluation of the models. 

There are various files in these archives: other than this README, each one can be identified by its filename, in the format {set}_{type}.{filetype}
- {set} refers to either train, dev, or test:
    train: You should use this data when building a model
    dev: You should use this data when evaluating a model
    test: You should submit the outputs on this data to Kaggle; the labels are not given
   
- {type} refers to either full, count, tfidf, glove300:
    full: This contains the raw text of the corresponding tweets, one tweet per line, in the following format:
          region,user,tweet (newline)
          where region is the class label (to be predicted), the User-ID identifies the author, and the Tweet-text the raw tweet

    count: For these files, we have pre-processed the corresponding tweets, and have recorded the term frequency for a subset of words (filtered by tfidf)
                    
    tfidf: For these files, we have pre-processed the corresponding tweets, and have recorded the tfidf (term frequency inverse document frequency) value a subset of words (pre-filtered by tfidf). 
    
    glove300: For these files, we have pre-processed the corresponding tweets, and have mapped each word to its pre-trained word embedding (GloVe) and averaged the embeddings of all words in the tweet

Finally, 'vocab.txt' contains the vocabulary after tfidf-filtering (underlying the count and tfidf files), mapping each word to a unique identifier (ID), of the form 
    word \tab ID (newline)

References: 
Eisenstein, J., O'Connor, B., Smith, N., and Xing, E. (2010). A latent variable model for geographic lexical variation. In Proceedings of the 2010 conference on empirical methods in natural language processing, pages 1277 - 1287.
