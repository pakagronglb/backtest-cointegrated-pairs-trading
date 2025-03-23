# Cointegrated Pairs Trading Strategy 🪙

![image](https://github.com/user-attachments/assets/ef388362-f92f-47a8-ad2d-9001d3fb3982)


![License](https://img.shields.io/badge/license-MIT-blue)
![Python](https://img.shields.io/badge/Python-3.7%2B-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-1.0%2B-brightgreen?logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-1.20%2B-lightblue?logo=numpy&logoColor=white)
![Statsmodels](https://img.shields.io/badge/Statsmodels-0.12%2B-orange)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.4%2B-yellow?logo=matplotlib&logoColor=white)
![yfinance](https://img.shields.io/badge/yfinance-0.1.70%2B-red)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google-Colab-yellow?logo=google-colab&logoColor=white)

## Overview 📝

This notebook implements a cointegrated pairs trading strategy following the Algovibes tutorial "[Cointegrated Pairs Trading](https://www.youtube.com/watch?v=qUMW9LEv4Qw)". The strategy identifies pairs of assets that are cointegrated, meaning their prices move together in the long term despite short-term deviations, and trades based on the mean-reversion of their price relationship.

## Features ✨

- Data retrieval using yfinance
- Testing for cointegration between asset pairs
- Calculation of hedge ratios using OLS regression
- Spread calculation and normalization
- Z-score based trading signal generation
- Strategy backtesting and visualization
- Performance metrics calculation

## Requirements ⚙️

- Python 3.7+
- pandas
- numpy
- statsmodels
- matplotlib
- yfinance
- scipy
- Google Colab or Jupyter Notebook

## Installation 📦

1. Open the Google Colab notebook:
   ```
   https://colab.research.google.com/drive/1BfrSyR51RUWzw52CKddczraji-OkE2Cf
   ```

2. The notebook includes all necessary package installations.

## Implementation Steps ⚙️

The notebook follows these key steps:

1. **Data Collection**: Fetches historical price data for selected asset pairs using yfinance
2. **Cointegration Testing**: Tests if the selected pairs are cointegrated using the Augmented Dickey-Fuller test
3. **Spread Calculation**: Computes the spread between the pairs using the calculated hedge ratio
4. **Z-score Normalization**: Normalizes the spread using rolling mean and standard deviation
5. **Signal Generation**: Creates trading signals when z-scores cross predefined thresholds
6. **Backtesting**: Simulates trading based on the signals and calculates returns
7. **Performance Analysis**: Evaluates strategy performance using metrics like cumulative returns, Sharpe ratio, and drawdowns

## Trading Logic 🧠

- **Entry Signals**:
  - When z-score exceeds upper threshold: Short the spread (short asset 1, long asset 2)
  - When z-score falls below lower threshold: Long the spread (long asset 1, short asset 2)
- **Exit Signals**:
  - Exit positions when z-score reverts to mean (crosses zero or predefined exit thresholds)

## Visualisation 👀

The notebook creates various visualizations:
- Price movements of the cointegrated pairs
- Spread and z-score time series
- Trading signals overlaid on z-score
- Cumulative returns of the strategy
- Drawdown analysis

## Credits 🙏🏻

This implementation is based on the tutorial by [Algovibes](https://www.youtube.com/watch?v=qUMW9LEv4Qw) on YouTube. Their excellent explanation of cointegrated pairs trading provided the foundation for this notebook.

## Further Improvements ✨

Potential enhancements to the basic strategy:
- Implementation of stop-loss mechanisms
- Dynamic threshold calculation
- Portfolio of multiple cointegrated pairs
- Transaction cost modeling
- Alternative cointegration tests and hedge ratio calculations

## License 📝

This project is licensed under the MIT License
