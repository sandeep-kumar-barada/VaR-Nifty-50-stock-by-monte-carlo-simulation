# VaR-Nifty-50-stock-by-monte-carlo-simulation

This repository implements a **Monte Carlo Simulation** for computing Value at Risk (VaR) of a stock using historical market data from Yahoo Finance.  
The implementation supports:
- **Normal distribution**
- **Student‑t distribution**
- **Historical simulation**
and uses a **fixed rolling window** for better performance and realistic risk estimation.

---

## 📌 Overview

**Value at Risk (VaR)** estimates the maximum loss expected over a defined period at a chosen confidence level.

This project:
- Fetches historical stock data with `yfinance`
- Calculates daily log returns
- Runs Monte Carlo simulations to estimate VaR at 95%, 99%, and 99.9% confidence levels
- Uses a fixed rolling window (default: 250 trading days)
- Supports multiple distribution models
- Plots VaR over time for easy visualization

---

## 🛠 Tech Stack

- **Python 3.x**
- Libraries:
  - `numpy`
  - `pandas`
  - `matplotlib`
  - `scipy`
  - `yfinance`

---

## 📦 Installation

Clone the repo and install dependencies:

