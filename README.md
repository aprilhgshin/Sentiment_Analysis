# Sentiment_Analysis of Social Media Towards Asian Ethnic Groups

## Introduction
This study presents a comprehensive analysis of sentiment on Asian ethnic groups all over the world. The social sentiment was conducted on tweets gathered from twitter during COVID-19's peak in April of 2020. The focus of this research is to shed light on the negative social impact that COVID-19 has had on Asians. The aim is to prove that negative sentiment exists, and to further educate people on the issue.

I compute the polarity (and normalized polarity) of tweets containing the hashtags *Coronavirus* and/or *Covid19*. Polarity will be based on vader's polarity scores.
Additionally, I investigate the polarity of tweets with Asian references.



## Methods:
- Cleaned dataset by the following:
  - Lowercase text
  - Remove words with backslash x
  - Remove website URLs
  - Removing links, special characters using simple regex statements
  - Remove stopwords

- Computed the polarity and normalized polarity scores of cleaned tweet texts using vader's polarity scores:
  - Polarity score is manually calculated using scores provided in vader's list of scores in vader_lexicon.txt
  - Normalized polarity score is calcuating using SentimentIntensityAnalyzer method from vaderSentiment.vaderSentiment module.

- Identified tweets with Asian reference and if user is a verified user:
  - Tweets with any of the keywords such as 'asian', 'asians', 'chinese', 'china', and 'wuhan' are considered to have an Asian reference.
  - Defined a 'verified' user to be a user with >= 9000 followers.

- Identified the top five tweets with most negative or positive polarity scores.

- Plotted the distributions and corresponding means of tweet polarities of various categories:
  - Tweets with and without Asian references
  - Tweets posted by 'verified' users vs 'normal' users

- Determined correlation between mean polarity scores and number of coronavirus cases in each US state:
  - Identified tweets with valid locations in the US (using major city and state names to determine tweet location)
  - Mapped polarity scores and number of coronavirus cases to corresponding locations on geopandas map of the US
  - Computed Pearson's correlation coefficient to study the strength of the linear relationship between the two variables
  - Computed Spearman's correlation coefficient to determine if there exists a nonlinear relationship between the two variables



## Resulting DataFrame with Polarity Scores:
The result is stored in DataFrame tweets_df with the following columns:

- timestamp
- tweet_text
- username
- all_hashtags
- followers_count
- location
- clean_text
- polarity
- normalized_polarity
- verified_user

