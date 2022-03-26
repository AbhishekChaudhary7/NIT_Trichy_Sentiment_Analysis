# NIT_Trichy_Sentiment_Analysis
## A one day fun project scrap the review from career360 of my college and do sentiment analysis on it and generate a roport.

## STEPS

### <-- Step1 -->---------------->>>SCRAPPING<<<
#### In this this step reviews has been scraped from career360, using BeautifulSoup library by html parser, HTML tags has also been carefully taken care of and after that exported into a xlsx file and saved

### <-- Step2 -->---------------->>>Normaliztion and Cleaning of Reviews<<<

In this step review has been first cleaned with the help of regex function and after that all sentences and words are converted to lower case.

### <-- Step3-->------------------>>>Tokenization<<<

#### In this step strings has been splited into smaller pieces or tokens with the help of nltk library

eg., The movie is good --> ['The', 'movie', 'is', 'good']

### <-- Step4-->------------------>>>Stemming<<<

#### Stemming is used to reduce words to their root from by removeing suffix chracters (As stemming is a rule based algorithm, it does not uses a dictionary), I have used PorterStemmer as it is not much aggresive like LancasterStemmer, and also mostly used.

eg., Learning --> learn,  Books --> Book, Caring --> Car (PS :- that is why stemming does not always provide the correct form)

### <<-- Step5-->--------------------->>>Removing Stop Words<<<
  
#### With the help of corpus module from nltk library stopwords which are not required are removed. and after that all the words which were in the form of token are joined.

eg., ['movie', 'good'] --> movie good

eg., The movie is good --> movie good (as 'The' and 'is' is not going to contribute the sentiment score)

### <<-- Step6-->--------------------->>>Sentiment Analysis<<<

#### With the help of TextBlob library sentiment subjectivity and polarity has generated and appended into a new column. and with that ordinal sentiment sentiment is generated. (if Score < 0 :- Negative and vice-versa and '0' for neutral) and then all analysis and score exported into a xlsx  file.

TextBlob generates this subjectivity and polarity score by using WordNet, which is completely mapped out english language. WordNet is completely lexical approach.
                                                            
                                                     


