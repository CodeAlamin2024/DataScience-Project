# DataScience-Project
# Analyzing Candle Range Theory (CRT) Trading Strategy

## Analyzing Trading Strategy Backtesting Data to Evaluate Performance and Predict Profitability

## Overview
This project applies data science techniques to evaluate the performance of a Forex trading system known as the Candle Range Theory (CRT). The main goal is to identify which factors influence trade profitability and whether the strategy demonstrates consistent, statistically measurable edges across different market conditions. The project follows an end-to-end data science pipeline from cleaning and preprocessing backtesting data to conducting exploratory data analysis (EDA), hypothesis testing, and building predictive models.

---

## Understanding the CRT Strategy
Candle Range Theory (CRT) is a price-action–based trading framework that analyzes how a sequence of larger candles (H4 timeframe) interacts with lower-timeframe behavior (M15). Rather than relying on traditional indicators, CRT focuses on market structure, liquidity, and candle dynamics.

## 1. The H4 → M15 Framework
CRT begins by identifying key candles on the 4-hour (H4) chart. The ranges—high, low, and body—of these candles act as important zones where institutions place orders. The strategy then drills down to the 15-minute (M15) chart to pinpoint precise entry points.

## 2. Candle 1 – Candle 2 – Candle 3 Model
The foundational pattern in CRT consists of three candles:
# Candle 1 (Impulse Candle):
Typically creates a large move that sweeps liquidity and sets the initial range.
# Candle 2 (Reversal Candle):
Often rejects the extreme of Candle 1 and signals a potential turning point.
# Candle 3 (Continuation Candle):
Confirms the direction by breaking out or filling imbalances.
Most CRT trades are based on the reaction around Candle 2.

## 3. Sweeps and Fair Value Gaps (FVG)
CRT relies heavily on two market behaviors:
Sweeps: Price briefly breaks a previous high/low to trigger stop losses before reversing.
Fair Value Gaps (FVGs): Areas where price moves too quickly, leaving temporary “imbalances” that tend to get filled.
A typical CRT entry involves waiting for a sweep or FVG tap around a key H4 candle level.

## 4. How a CRT Trade Works (Simplified)
1. Identify the active H4 candle of the day.
2. Detect a sweep or reversal formation between Candle 1 and Candle 2.
3. Switch to the M15 chart to refine entry timing using sweeps or FVG fills.
4. Enter at the imbalance or sweep zone; place stop-loss outside structure.
5. Target expected continuation from Candle 3.

## 5. Why CRT Is Suitable for Data Science
CRT is rule-based, structured, and time-dependent. This makes it ideal for data-driven evaluation:
- Clear entry and exit rules
- Time-based hierarchy (H4 → M15)
- Repeatable patterns
- Zones that can be converted into numerical features
This allows the CRT strategy to be examined using statistical tests and machine learning.

## Motivation
Traders often rely on intuition or experience, but markets generate rich data that can be analyzed objectively. As a data science student and trader, I wanted to answer:
> “Which parts of the CRT strategy truly produce an edge and which do not?”
Backtesting provides a controlled environment where trades can be studied without emotional influence. This project combines financial logic with data science methodology to validate or challenge assumptions about the strategy.

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

### Author
### **Name:** Alamin Bawa Idris
### **Course:** DSA 210 — Introduction to Data Science by Özgür Asar
### **Term:** 2025–2026 Fall  
### **Institution:** Sabanci University  

---

> *“Trading is where data meets psychology, and Data Science gives us the language to understand both.”*
