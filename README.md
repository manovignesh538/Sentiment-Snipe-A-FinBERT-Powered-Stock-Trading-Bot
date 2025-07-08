# 📈 Sentiment Snipe: A FinBERT-Powered Stock Trading Bot

Sentiment Snipe is an intelligent trading bot that analyzes the **sentiment of real-time stock news** using **FinBERT** and automatically places **BUY/SELL** orders through **Alpaca's trading API**. The bot makes precise decisions by "sniping" high-confidence trades based on positive or negative news, making it ideal for sentiment-driven momentum trading.

---

## 🚀 Features

- 🧠 **FinBERT-Powered Sentiment Analysis**  
  Uses `ProsusAI/finbert` transformer to evaluate financial news sentiment (positive, negative, neutral).

- 🔍 **Live News Integration**  
  Pulls the latest headlines for a selected stock using Alpaca’s `get_news` API.

- 💹 **Auto-Trading with Alpaca**  
  Places market orders to buy/sell based on confidence level from sentiment analysis.

- 📊 **Rich Visualizations**  
  Includes advanced plots like sentiment pie chart, word clouds, and price overlays for insight and presentation.

- ⏱️ **Smart Decision Logic**  
  Executes trades only when confidence > 90% — avoids noise and prevents false signals.

---

## 📷 Sample Output

| Sentiment Distribution | Word Cloud |
|------------------------|------------|
| ![Pie](assets/sentiment_pie.png) | ![WordCloud](assets/wordcloud.png) |

---

## 🛠️ Tech Stack

| Tool           | Purpose                             |
|----------------|-------------------------------------|
| **Python**     | Core logic and execution            |
| **FinBERT**    | Sentiment analysis using Transformers |
| **Alpaca API** | Brokerage integration for trading   |
| **Matplotlib / Seaborn** | Visual plots and insights |
| **Jupyter Notebook** | Interactive development environment |
| **LumiBot (Optional)** | Algo trading framework (explained but not used due to market hours) |

---

## 🧪 Strategy Logic

```python
if sentiment == "positive" and confidence > 0.90:
    place_buy_order()
elif sentiment == "negative" and confidence > 0.90:
    place_sell_order()
else:
    skip_trade()
