# 📈 Sentiment Snipe: AI-Powered Stock Trading Bot using FinBERT, Alpaca & LumiBot

**Sentiment Snipe** is a smart stock trading bot that uses real-time financial news and AI to decide **when to BUY or SELL stocks**. Powered by **FinBERT** for sentiment analysis, **Alpaca** for brokerage, and **LumiBot** for live and backtest-ready trading strategy design — this project bridges the gap between NLP and algorithmic trading.

---

## 🚀 Features

- 🧠 **FinBERT-Based Sentiment Analysis**  
  Uses a finance-specific BERT model (`ProsusAI/finbert`) to classify news into positive, negative, or neutral sentiment.

- 📰 **Live Financial News Feed**  
  Automatically fetches headlines for a given stock from Alpaca's news API.

- 💹 **Automatic Buy/Sell Execution**  
  Trades are only executed when confidence is high — reducing risk from noise.

- ⚙️ **LumiBot Strategy Integration**  
  Strategy logic is written and demonstrated using LumiBot — a professional algo trading framework.

- 📊 **Professional Visualizations**  
  Includes sentiment pie charts, word clouds, price-sentiment overlays, and heatmaps.

---

## 🔧 Tools & Technologies

| Tool         | Purpose                              |
|--------------|---------------------------------------|
| `FinBERT`    | News sentiment analysis               |
| `Alpaca API` | Broker execution (paper trading)      |
| `LumiBot`    | Strategy framework for trading logic  |
| `Python`     | Main programming language             |
| `Matplotlib`, `Seaborn` | Visualizations             |
| `Jupyter Notebook` | Interactive development         |

---

## 🧠 Strategy Logic

```python
if sentiment == "positive" and confidence > 0.90:
    place_market_buy()
elif sentiment == "negative" and confidence > 0.90:
    place_market_sell()
else:
    skip_trade()
