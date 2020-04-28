# Sentiment_Analysis of Social Media Towards Asian Ethnic Groups

## Introduction
This study presents a comprehensive analysis of sentiment on Asian's all over the world. The social sentiment was conducted on tweets gathered from twitter during COVID-19's peak in April of 2020. The focus of this research is to shed light on the negative social impact that COVID-19 has had on Asians. The aim is to prove that negative sentiment exists, and to further educate people on the issue.

We compute the polarity (and normalized polarity) of tweets containing the hashtags *Coronavirus* and/or *Covid19*.
Polarity will be based on vader's polarity scores.
Additionally, we investigate the polarity of tweets with a reference to asian ethnic groups.

Tweet texts will be cleaned by setting all characters to lowercase and removing words with backslash x, stopwords, links, and special characters using simple regex statements. 

The result will be stored in DataFrame *tweets_df* with the following columns:
- timestamp
- tweet_text
- username
- all_hashtags
- followers_count
- location
- clean_text
- polarity
- normalized_polarity

