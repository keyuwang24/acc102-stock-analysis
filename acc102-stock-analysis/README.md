# Stock Technical Analysis Tool - RSI & MACD Backtesting

## 1. Problem & User

**Problem**: Beginner investors struggle to identify stock entry/exit points. Technical indicators like RSI are difficult to calculate manually.

**Target User**: Investment beginners who want to understand how technical indicators work through historical backtesting.

**What this project does**: Downloads stock data from WRDS (CRSP), calculates RSI indicator, generates buy/sell signals, and evaluates historical performance.

## 2. Data Source

- **Source**: WRDS (CRSP database)
- **Ticker**: AAPL (Apple Inc.)
- **Time Period**: April 2024 - April 2026
- **Access Date**: April 18, 2026

## 3. Methods (Python workflow)

1. **Data Acquisition**: WRDS connection via Python `wrds` library
2. **Data Cleaning**: Check for missing values
3. **Indicator Calculation**: RSI (Relative Strength Index) - 14-day period
4. **Signal Generation**: RSI < 30 → Buy signal
5. **Performance Evaluation**: Calculate 5-day and 10-day forward returns
6. **Visualization**: Matplotlib charts

## 4. Key Findings

- RSI generated 18 buy signals during the 2-year analysis period
- Average 5-day return after RSI buy signal: **+0.88%**
- Average 10-day return after RSI buy signal: **-0.18%**
- 10-day win rate: **55.6%**
- No MACD golden cross signals occurred in this period

## 5. How to Run

### Requirements
```bash
pip install -r requirements.txt