#  Sentiment-Aware Trader Intelligence System

##  Overview
This project analyzes the relationship between Bitcoin market sentiment and trader performance using behavioral modeling, clustering, and strategy evaluation.

The goal is to uncover whether sentiment can be used to improve trading strategies and to identify different types of traders based on their behavior.

---

##  Datasets Used
- Bitcoin Fear & Greed Index
- Historical Trader Data (Hyperliquid)

---

##  Methodology

### 1. Data Cleaning
- Standardized column names
- Converted UNIX timestamps to datetime
- Removed invalid/system-generated trades

### 2. Feature Engineering
- Return Percentage → normalized performance
- Risk Score → exposure-adjusted volatility
- Trade Outcome → win/loss classification

### 3. Trader-Level Analysis
Aggregated trader behavior:
- Average return
- Risk profile
- Trading activity
- Total PnL

### 4. Discipline Score (Custom Feature)
Designed a composite score combining:
- Returns (reward)
- Risk (penalty)
- Overtrading (penalty)

### 5. Trader Clustering
Used K-Means to identify trader archetypes:
- High-risk traders
- Professional traders
- Overtraders
- Balanced traders

### 6. Sentiment Analysis
- Merged sentiment with trade data
- Evaluated performance across sentiment regimes

### 7. Strategy Evaluation
Tested a sentiment-based strategy:
- Trade aggressively during fear
- Reduce exposure during greed

---

##  Key Findings

- Greed phases show higher average returns
- Sentiment impacts trader behavior but is not a reliable standalone signal
- Professional traders outperform across varying conditions
- High-risk traders generate extreme but inconsistent returns
- Naive sentiment-based strategies underperform baseline trading

---

##  Conclusion

Market sentiment provides useful context but is insufficient for building profitable strategies alone.

Combining sentiment with behavioral modeling yields deeper insights into trader performance.

---

##  Tech Stack
- Python
- Pandas, NumPy
- Scikit-learn (KMeans)
- Matplotlib, Seaborn

---

##  Future Improvements
- Incorporate time-series models (LSTM/Transformers)
- Add transaction cost modeling
- Use reinforcement learning for strategy optimization
