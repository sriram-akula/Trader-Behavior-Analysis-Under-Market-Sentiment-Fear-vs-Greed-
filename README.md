# Trader Behavior Analysis Under Market Sentiment (Fear vs Greed)

## Overview

Financial markets are heavily influenced by investor sentiment. Periods of market fear often correspond with high volatility, while greed reflects optimism and potentially overconfident trading behavior.

This project analyzes how market sentiment (Fear vs Greed) influences trader behavior and performance on the Hyperliquid trading platform.

By combining historical trader transaction data with Bitcoin Fear & Greed Index data, the analysis investigates whether traders change their behavior, risk-taking patterns, and performance depending on market sentiment.

The goal is to uncover behavioral patterns that could help inform smarter trading strategies.

---

# Dataset

Two datasets were used for this analysis.

## 1. Bitcoin Market Sentiment Dataset

This dataset contains the Bitcoin Fear & Greed Index which reflects overall market sentiment.

Columns include:

- date
- classification (Fear, Greed, Extreme Fear, Extreme Greed, Neutral)
- value (index value)

This dataset provides a daily snapshot of market sentiment.

---

## 2. Historical Trader Data (Hyperliquid)

This dataset contains detailed trading activity.

Columns include:

- Account
- Coin
- Execution Price
- Size Tokens
- Size USD
- Side (BUY / SELL)
- Timestamp IST
- Direction
- Closed PnL
- Fee
- Trade ID
- Transaction Hash

Each row represents an individual trade executed by a trader.

---

# Methodology

The analysis was performed in several stages.

## 1. Data Cleaning

- Loaded both datasets using Python (Pandas).
- Checked dataset dimensions.
- Verified missing values and duplicates.
- Converted timestamp fields into datetime format.
- Extracted daily date values to align both datasets.

## 2. Dataset Integration

The trader dataset was merged with the sentiment dataset using the date field so that each trade could be associated with the prevailing market sentiment.

Final merged dataset:

**211,224 trading records with sentiment information.**

---

## 3. Feature Engineering

Several behavioral metrics were created to analyze trader behavior.

Metrics included:

- Daily PnL per trader
- Number of trades per day
- Average trade size (USD)
- Win rate
- Long vs Short ratio
- Trading volume
- PnL volatility (risk proxy)

These metrics help evaluate trader activity, profitability, and risk-taking behavior.

---

# Analysis

The analysis focuses on understanding how trader performance and behavior differ across sentiment regimes.

The following comparisons were performed:

- Trader profitability across sentiment regimes
- Trading activity levels across sentiment regimes
- Position sizing behavior
- Long vs short trading bias

Visualization tools such as Matplotlib and Seaborn were used to create charts supporting the analysis.

---

# Key Insights

## Insight 1 — Fear Dominates Trading Activity

The dataset shows that the majority of trades occur during **Fear market conditions**, indicating traders tend to be more active during volatile or uncertain market environments.

Higher volatility likely creates more short-term trading opportunities.

---

## Insight 2 — Market Sentiment Influences Trading Behavior

Trading activity, position sizes, and directional bias vary depending on market sentiment.

This suggests that trader behavior is strongly influenced by overall market psychology.

---

## Insight 3 — Profitability and Risk Vary Across Sentiment Regimes

Periods of Fear show greater variability in PnL outcomes, indicating both higher risk and higher reward potential compared to Greed periods.

---

# Strategy Recommendations

Based on the analysis, the following trading strategies are suggested.

## Strategy 1 — Volatility Exploitation During Fear

During Fear periods:

- Monitor market volatility closely
- Increase trading activity cautiously
- Focus on short-term opportunities

Fear-driven volatility may create profitable trading conditions.

---

## Strategy 2 — Risk Management During Greed

During Greed periods:

- Reduce excessive risk-taking
- Avoid overleveraged positions
- Focus on disciplined trading strategies

Greed markets may lead to overconfidence and potential market corrections.

---

# Bonus Section (Optional)

A simple machine learning model was implemented to predict whether a trade results in positive PnL using features such as:

- trade size
- execution price
- sentiment
- trade direction

This demonstrates how behavioral and sentiment indicators can be used in predictive trading models.

---

# Technologies Used

Python  
Pandas  
NumPy  
Matplotlib  
Seaborn  
Scikit-Learn

---

# How to Run the Project

1. Clone the repository

2. Install required libraries

3. Open the notebook

4. Run all cells to reproduce the analysis.


