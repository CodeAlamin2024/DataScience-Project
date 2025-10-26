# DataScience-Project
# Analyzing Candle Range Theory (CRT) Trading Strategy

## Analyzing Trading Strategy Backtesting Data to Evaluate Performance and Predict Profitability

## Overview
This project applies data science methodologies to analyze trading strategy backtesting data. The goal is to identify which factors most strongly influence profitability and risk while developing predictive understanding for future trades. It demonstrates how data-driven approaches can enhance trading decision-making and strategy optimization.

---

## Motivation
As both a trader and data science student, I aim to understand how quantitative metrics reflect trading performance.  
Backtesting data provides a perfect foundation for applying the data science process from data collection to machine learning.  
Through this project, I hope to answer a key question:

> “What makes a trading strategy consistently profitable over time?”

---

## Data Source
**Primary Dataset:**  
Backtesting results from my personal trading strategies tested on historical Forex market data.

Each record in the dataset includes:
- Date and time of trade  
- Entry and exit prices  
- Trade direction (Buy/Sell)  
- Profit or loss amount  
- Stop-loss and take-profit levels  
- Technical indicators that triggered the trade (e.g., RSI, Moving Average, MACD)

**Collection Method:**  
Data is generated via a platform-based backtesting system (TradingView). To enrich this dataset (as required), I will integrate additional financial indicators such as:
- Daily volatility or ATR values  
- Major economic news events (e.g., CPI, NFP releases)  
- Market session information (London, New York, Asian sessions)

---

## Methodology

### 1. **Data Cleaning & Preparation**
- Handle missing or incomplete trade entries  
- Convert timestamps to extract features (hour, weekday, session)  
- Normalize profit/loss values  
- Create new features such as risk–reward ratio, duration, and volatility exposure  

### 2. **Exploratory Data Analysis (EDA)**
- Profit and loss distribution visualization  
- Win-rate trends by day, session, or indicator  
- Correlation between features (e.g., indicator signals vs. profitability)  
- Time-series analysis of equity growth  

### 3. **Hypothesis Testing**
- Test if performance differs significantly between trading sessions or market conditions  
- Examine whether higher risk correlates with higher average returns  

### 4. **Machine Learning Application**
Goal: Predict **whether a trade will be profitable** based on pre-trade features.  
Models considered:
- Logistic Regression / Random Forest (classification)  
- Linear Regression / XGBoost (return prediction)  
- Feature importance analysis for signal interpretation  

---

## Expected Findings
- I want to understand which technical factors most strongly correlate with profitability  
- Understanding of how market timing affects trade outcomes  
- A model capable of estimating the probability of success before a trade executes  
- Visualized performance metrics (equity curve, drawdown, Sharpe ratio, etc.)

---

## Tools Used
| Category | Tools |
|-----------|--------|
| Language | Python |
| Data Handling | pandas, numpy |
| Visualization | matplotlib, seaborn, plotly |
| Machine Learning | scikit-learn, statsmodels |
| Version Control | GitHub |
| Documentation | Jupyter Notebook, Markdown |

All dependencies will be listed in `requirements.txt`.

---

## Limitations & Future Work
- The dataset is derived from historical backtests and does not reflect real-time liquidity or slippage.  
- Sentiment and macroeconomic data are partially integrated.  
- Future steps:
  - Extend to real-time data validation  
  - Incorporate deep learning models for predictive trade filtering  
  - Build an interactive dashboard for live visualization
 
---

## Deliverables
- Python scripts for data cleaning, analysis, and modeling  
- Visualizations (profit curve, correlation plots, etc.)  
- Report 
- `requirements.txt` for dependencies  
- `README.md`  

---

## Ethical Considerations
- My data is simulated and derived from open financial sources. 
- External datasets (e.g., economic indicators) will be properly cited.  
- AI tools such as ChatGPT were used for proposal structuring and documentation, with full disclosure in compliance with academic integrity policies.

---

## Author
## **Name:** Alamin Bawa Idris
## **Course:** DSA 210 — Introduction to Data Science by Özgür Asar
## **Term:** 2025–2026 Fall  
## **Institution:** *Sabanci University*  

---

> *“Trading is where data meets psychology, and data science gives us the language to understand both.”*
