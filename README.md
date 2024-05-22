# Stock-Sentiment-Analysis

Models used:
1) Support Vector Regression
2)Random Forest

We have performed sentiment analysis of the twitter data based on a whole day as well as based on an hourly basis to analyze the effect it has on stock market prediction
The models are evaluated and compared using RMSE (root mean squared error) values

The steps involved are:
1.**Data Collection using yfinance API** :Tweets on Microsoft, Google, AAPL, are extracted. The tweets will have
collected using Twitter API and filtered using keywords like $ MSFT, # Microsoft,
#Windows etc. Not only the opinion of public about the company’s stock but also the
opinions about products and services offered by the company.

2. **Data Preprocessing and Removal of Null Values** :Stock prices data collected is not complete understandably because of weekends and public
holidays when the stock market does not function. The missing data is approximated using a
simple technique. Stock data usually follows a concave function. So, if the stock value on a
day is x and the next value present is y with some missing in between. The first missing value
is approximated to be (y+x)/2 and the same method is followed to fill all the gaps

**Tokenization**: Tweets are split into individual words based on the space and irrelevant
symbols like emoticons are removed. We form a list of individual words removed. Form
a list of individual words for each tweet
 **Stop word Removal**: Words that do not express any emotion are called Stop words. After
splitting a tweet, words like a, is, the, with etc. are removed from the list of words. 

**Sentiment Analysis** :Sentiment analysis task is very much field specific. Tweets are classified as positive, negative
and neutral based on the sentiment present. Out of the total tweets are examined by humans
and annotated as 1 for Positive, 0 for Neutral and 2 for Negative emotions

**Feature Extraction** :Textual representations can be done using n-grams. N-gram Representation: N-gram
representation is known for its specificity to match the corpus of text being studied. In these
techniques a full corpus of related text is parsed which are tweets in the present work, and
every appearing word sequence of length n is extracted from the tweets to form a dictionary
of words and phrases

7. **Applying Regression Models**:The features extracted using the above methods for the tweets are fed to the classifier and
trained using classification methods like Random FDorest Regression and Support Vector Machine
to estimate the movement of the change in stock market price vs the volume as well as
sentiment of news articles and tweets.

![image](https://github.com/galactic-me/Stock-Sentiment-Analysis/assets/126558668/49f5dbf2-afab-473e-92cf-f505d0429a71)

