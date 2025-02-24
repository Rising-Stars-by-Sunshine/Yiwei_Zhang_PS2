This repository contains a financial-domain-focused dataset for financial sentiment/emotion classification and stock market time series prediction. It's an open access dataset comes from the paper: [StockEmotions: Discover Investor Emotions for Financial Sentiment Analysis and Multivariate Time Series](https://arxiv.org/abs/2301.09279) accepted by AAAI 2023 Bridge (AI for Financial Services).


## Key statistics of the data<img width="1028" alt="截屏2025-02-24 08 58 54" src="https://github.com/user-attachments/assets/f0af49f2-565c-4b17-b457-cb6fbf9683dd" />

- Data collection period : **Jan 2020 - Dec 2020**
- Number of Utterance : **10,000**  (train 80%, val 10%, test 10%)
- Sentiment classes: 2 annotated by users 
    - **bullish** (~positive), **bearish** (~negative)
- Emotion classes: 12 annotated by Human & AI collaboration
    - **ambiguous, amusement, anger, anxiety, belief, confusion, depression, disgust, excitement, optimism, panic, surprise** 
<p align="left"><img src="./img/4_annotation_guide.png" style="max-width: 40%;"></p>

[Download the dataset](./data/stock_data.csv)

## Data explained
- tweet folder
    - **processed.csv**: 50,281 samples with text processed data (handling emoji and CTAG). It is used for Topic Modelling before proceeding with the emotion annotation.
    - **train, val, test.csv** : In total, 10,000 samples. Each file has id, date, ticker, emo_label, senti_lable, original, and processed content. For the data curation, processing (e.g. emoji, CTAG, HTAG), and annotation, we refer to our paper. The dataset is used for Financial Sentiment/Emotion Classification tasks. 
- price folder
    - **38 companies histrical price data** in csv format. The tweet and price dataset together are used for Multivariate Time Series tasks. 
    - Tickers: 
        'AAPL', 'ABNB', 'AMT', 'AMZN', 'BA', 'BABA', 'BAC', 'BKNG', 'BRK.A', 'BRK.B', 'CCL', 'CVX',
        'DIS', 'FB', 'GOOG', 'GOOGL', 'HD', 'JNJ', 'JPM', 'KO', 'LOW', 'MA', 'MCD', 'MSFT', 'NFLX',
        'NKE', 'NVDA', 'PFE', 'PG', 'PYPL', 'SBUX', 'TM', 'TSLA', 'TSM', 'UNH', 'UPS', 'V', 'WMT', 'XOM'
        - 'FB' ticker is changed to 'META', but the time at the data collection was 'FB'.

