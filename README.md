# Sentiment_Analysis

We compute the polarity (and normalized polarity) of tweets containing the hashtags *Coronavirus* and/or *Covid19*.
Polarity will be based on vader's polarity scores.

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

