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
Steps

1. Clone this repository
2. Open notebook.ipynb in Jupyter Notebook
3. Run all cells sequentially (you need WRDS credentials)
4. Charts will be saved to figures/ folder

```

## 6. Project Structure

acc102-stock-analysis/
├── notebook.ipynb          # Main analysis file
├── README.md               # This file
├── requirements.txt        # Dependencies
└── figures/                # Output charts
    ├── rsi_analysis.png
    └── macd_analysis.png
```

##  7. Demo Video

[Link to your Mediasite demo video]

##  8. Limitations

· Single stock analysis (AAPL only)
· WRDS access required to run the code
· No transaction costs considered
· MACD analysis limited by zero signals

##  9. Author

Keyu Wang - ACC102 Mini Assignment, April 2026
