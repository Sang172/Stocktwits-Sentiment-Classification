# stocktwits_sentiment_classification
This repository is some of the codes I used for a group project at Stanford's machine learning class (CS 129) in winter 2024.
It classifies Stocktwits messages into either positive, neutral, negative, or spam using BERT.
Stocktwits is a social media platform similar to X (formerly twitter) that focuses on the discussion of stocks and is widely used by the retail investor community.

stocktwits_scrape.ipynb scrapes Stocktwits messages using classes and functions defined in the src folder (parser.py, scraper.py, utils.py) given the list of tickers (microcap.csv).
For each ticker, I retrieve the most recent 100 messages on Stocktwits that tag the ticker, which resulted in around 80,000 messages (stocktwits_scraped.csv).
2,000 messages were randomly selected, manually labelled (labelled_bert.csv), and used to train the BERT model in bert_clean.ipynb.

The trained BERT model was then used to classify the remaining messages (bert_train_lablled.csv).
The model had 81.4% accuracy, 66.7% preicision, and 65.4% recall.
