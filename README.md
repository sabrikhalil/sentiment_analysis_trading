# **Sentiment-Driven Stock Strategy**

The idea of the work here is to trade based on sentiment analysis of headlines on the news, we use Apple stock here for test. 

Basically, we use NLP models to get a score per each day from the headlines, and we buy when the sentiment is more positive and sell when it becomes negative. We use Backtrader to test the strategy on that period of time, and see the results. 

I share the Notebook in this github: 

## 1. Import all Data needed (Stock price of Apple + Headline)

- Fetch Apple daily stock market value
- Fetch Apple headlines for the last 30 days

## 2. Using a Finance-Tuned Sentiment Model (NLP)

- Apply sentiment analysis to the headlines
- Merge/integrate sentiment scores with the price DataFrame

## 3. Use Backtrader to run a trading strategy based on the sentiment data

- Prepare the custom Pandas feed (`SentPandas`) — is how Backtrader works, to feed him data.
- Define the EMA-sentiment strategy class (`SentEMAStrat`) — we buy when EMA is higher than a threshold and sell when it's lower than a threshold.
- Run the backtest and visualize results
- Compare strategy’s returns to a buy-and-hold benchmark
