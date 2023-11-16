# Project-2
DigitalBhem Project 2


1.Information:
Twitter is one of the platforms widely used by people to express their opinions and showcase sentiments on various occasions. Sentiment analysis is an approach to analyze data and retrieve sentiment that it embodies.The tweet format is very small, which generates a whole new dimension of problems like the use of slang, abbreviations, etc. This analysis reports on the exploration and preprocessing of data, transforming data into a proper input format and classify the user’s perspective via tweets into positive(non-racist) and negative (racist) by building supervised learning models using Python and NLTK library.Formally, given a sample of tweets and labels, where label '1' denotes the tweet is racist/sexist and label '0' denotes the tweet is not racist/sexist, our objective is to predict the labels on the test dataset.


2.Import Modules:

-Importing Regular Expression (re) and we will using this to find a particular phrases Or to replace the particular phrases Or words.

-To do some pre-processing, we're using the string module.

-To understand people's sentiments, we are using Natural Language Toolkit(NLTK) Module.


3.Loading Dataset


4.Pre-Processing Dataset:

-A vectorize means , it will pass each row to this bellow function and it will give the expecting output.

-"\w" returns a match where the string contains any word character (Characters from a to z , digits form 0-9 , and the underscore_character)

-"*" Means Zero or More Occurrences.

-Removing some special characters numbers and punctuvations.

-"[^a-zA-Z#]" returns a match for only character except lower & upper alphabets ,Hashtag(#).

-Steming words we are using PorterStemmer , like this we have so many techniques like lemmantization stemming(WordNetLemmatizer) of NLP preprocessing.

-Stemming , it will just narrow down into a single common wod. for example lets say {"fighting","fight","fighter"} , this all words will be stemmed into "fight".


5.Exploratory Data Analysis


6.Input Split:

-True Positive:
    Interpretation: You predicted positive and it’s true.You predicted that a Tweet is not racist and Tweet actually is.

-True Negative:
    Interpretation: You predicted negative and it’s true.You predicted that a Tweet is racist and Tweet actually is.

-False Positive: (Type 1 Error)
    Interpretation: You predicted positive and it’s false.You predicted that a Tweet is not a racist but Tweet is actually is racist.

-False Negative: (Type 2 Error)
    Interpretation: You predicted negative and it’s false.You predicted that a Tweet is racist but Tweet actually is not racist.

-Precision:
    It is implied as the measure of the correctly identified positive cases from all the predicted positive cases. Thus, it is useful when the costs of False Positives is high.
    
    Precision = True Positive / (True Positive + False Positive)

-Recall:
    It is the measure of the correctly identified positive cases from all the actual positive cases. It is important when the cost of False Negatives is high.
    
    Recall = True Positive / (True Positive + False Negative)

-Accuracy:
    One of the more obvious metrics, it is the measure of all the correctly identified cases. It is most used when all the classes are equally important.
    
    Accuracy = True Positive +True Negative / (True Positive + False Positive + True Negative + False Negative)

-F1 score:
    This is the harmonic mean of Precision and Recall and gives a better measure of the incorrectly classified cases than the Accuracy Metric.
    
    F1 Score = ( 2 * Precision * Recall ) / (Precision + Recall)

-Note:
    
    1. Accuracy is used when the True Positives and True negatives are more important while F1-score is used when the False Negatives and False Positives are crucial
    2. Accuracy can be used when the class distribution is similar while F1-score is a better metric when there are imbalanced classes.
    3. In most real-life classification problems, imbalanced class distribution exists and thus F1-score is a better metric to evaluate our model on.


7.Model Training:

-Logistic Regression.

Logistic Regression is a classification algorithm could help us predict whether the given Tweet is Racist or not. Logistic regression predictions are distinct. We can also view probability scores underlying the model’s classifications.

-Naive Bayes

Naive Baye is a classification technique based on the Bayes’ Theorem with an assumption of independence among predictors. Bayes’ Theorem provides a way in which an equation is describing the relationship of conditional probabilities of statistical quantities. In Bayesian classification, we’re interested in finding the probability of a label given some observed features.
