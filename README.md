# Historical VaR and CVaR Analysis

Python notebook for estimating Value at Risk (VaR) and Conditional Value at Risk (CVaR) on an ETF portfolio using the historical simulation approach.

The project was developed in Google Colab and retrieves market data from Yahoo Finance through `yfinance`.

## Overview

The notebook performs the following steps:

1. Downloads 15 years of historical data for a basket of ETFs:
   - `EXS1.DE` - DAX exposure
   - `CSMIB.MI` - FTSE MIB exposure
   - `SXRW.DE` - FTSE 100 exposure
   - `CSSPX` - S&P 500 exposure
2. Computes daily log returns.
3. Builds an equally weighted portfolio.
4. Aggregates returns over an `N`-day horizon, with one day as the default.
5. Estimates VaR and CVaR in absolute monetary terms.
6. Visualizes the return distribution, highlighting VaR and CVaR thresholds.

## Methodology

Historical VaR estimates the portfolio loss threshold directly from the empirical return distribution, without assuming normally distributed returns.

CVaR, also known as Expected Shortfall, measures the average loss beyond the VaR threshold and provides a clearer view of tail risk.

## Requirements

```bash
pip install numpy pandas yfinance matplotlib
```

## Scope

This is an educational risk-management notebook. It focuses on historical simulation and portfolio-level tail-risk visualization, not on a full production risk engine with backtesting, stress scenarios or regulatory reporting.
