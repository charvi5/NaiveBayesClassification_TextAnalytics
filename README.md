
Description
-------------------------------------------------------------------------------------------------------------------------
A job description corpus along with salary for the job descriptions were used to build a classification model. This is done to predict the probability of a salary being above 75th quantile of data provided based on job descriptions.  

Notes
-------------------------------------------------------------------------------------------------------------------------
- The code has been written used Python3 using Jupiter notebook as interface

- The code needs to be executed in a sequential fashion as in certain case previously created tables are referred to later

**Approach**
------------------------------------------------------------------------------------------------------------------------
For job description corpus, basic data pre-processing steps such as stemming, lemmatization, stopword removal were employed.   
To analyze the description corpus and build a classification model, [TFIDF](https://en.wikipedia.org/wiki/Tf%E2%80%93idf) vectorizer was employed to give lower weights to words with higher frequency in job description corpus as an initial step.  
The salaries were then classified using [Multinomial Naive Bayes](https://en.wikipedia.org/wiki/Naive_Bayes_classifier#Multinomial_naive_Bayes) classification which showed an accuracy of 76%.  For performance comparison, freuqncy distance was calculated between words and top 1000 words were selected. A [Binomial Naive Bayes](https://en.wikipedia.org/wiki/Naive_Bayes_classifier) was then run on the words for classification which gave an almost equivalent accuracy of 74%. 
For further improvement, the analysis was run again by including bigrams of words. The accuracy remained same unexpectedly. 

Installing libraries and packages
-----------------------------------------------------------------------------------------------------------------------
To run the notebook, following list of packages must be installed in the system:
-  Pandas
-  Numpy
-  nltk
-  re
-  matplotlib
-  collections
-  itertools
-  sklearn

**nltk** is a Natural Language toolkit and is used for natural language processing. Following libraries need to be imported form the toolkit:  
- ```from nltk.corpus import brown```
- ```from nltk.corpus import stopwords```
- ```from nltk.stem import WordNetLemmatizer```
- ```from nltk.classify.scikitlearn import SklearnClassifier```

**Mac OS:**
- To download libraries and packages being loaded in first block of the code, go to Terminal and download packages using 
```pip install package-name ```
- If pip throws an error due to packages not being a part of pip anymore, use ```conda install package-name``` , this is an Anaconda command and directly downloads packages in Anaconda . 

**Windows:**
- Open Windows command prompt and enter ```py -3.6 -m pip install package-name```

-------------------------------------------------------------------------------------------------------------------------



