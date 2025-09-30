# Historic VaR – Value at Risk Analysis with Python

This project implements a simple **Value at Risk (VaR)** and **Conditional Value at Risk (CVaR)** analysis using the **historical approach** on a portfolio of ETFs.  
The notebook was developed in **Google Colab** and retrieves data directly from **Yahoo Finance** using the `yfinance` library.

---

## Overview
The notebook performs the following steps:
1. **Download historical data** (last 15 years) for a basket of selected ETFs:
   - `EXS1.DE` (MSCI Emerging Markets)  
   - `CSMIB.MI` (FTSE MIB)  
   - `SXRW.DE` (MSCI World)  
   - `CSSPX` (S&P 500)  
2. **Compute daily log returns**.  
3. **Build the portfolio** with equal weights.  
4. **Aggregate returns over N-day periods** (default: 1 day).  
5. **Calculate Value at Risk (VaR)** and **Conditional VaR (CVaR)** in absolute monetary terms (€).  
6. **Visualize the results** with a histogram of portfolio returns highlighting VaR and CVaR.  

---

## Requirements
Make sure you have the following Python libraries installed:

```bash
pip install numpy pandas yfinance matplotlib
