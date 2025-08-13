# VaR-Nifty-50-stock-by-monte-carlo-simulation
Monte Carlo Value at Risk (VaR) Simulation
This repository contains a Python implementation of Monte Carlo Simulation for Value at Risk (VaR) estimation using historical stock price data from Yahoo Finance.
The code calculates VaR at different confidence levels (95%, 99%, 99.9%) and visualizes its evolution over time.

📌 Project Overview
Value at Risk (VaR) is a widely used risk metric in finance that estimates the maximum expected loss over a given time period at a specific confidence level.
In this project, we use Monte Carlo simulation to forecast possible returns and derive VaR from the simulated distribution.

We:

Fetch historical stock price data using yfinance

Calculate daily log returns

Simulate potential future returns using a Normal distribution

Compute VaR for 95%, 99%, and 99.9% confidence levels

Track VaR changes over an expanding time window

Visualize the time series of VaR

🛠️ Technologies Used
Python 3.x

Jupyter Notebook

Libraries:

numpy

pandas

yfinance

matplotlib

scipy.stats

📂 Project Structure
text
Monte_Carlo-VaR.ipynb   # Main notebook containing data fetching, simulation, and plotting
README.md               # Documentation
⚙️ How It Works
Data Fetching

Retrieve historical daily prices for a given ticker (e.g., TATAMOTORS.NS) for a chosen date range using yfinance.

Log Return Calculation

Convert percentage change into daily log returns:

log_return
t
=
ln
⁡
(
P
t
P
t
−
1
)
log_return 
t
 =ln( 
P 
t−1
 
P 
t
 
 )
Simulation Process

Start with a minimum history window (e.g., first 101 trading days), then expand the dataset each iteration.

For each iteration:

Compute historical mean (μ) and standard deviation (σ) of log returns.

Simulate N possible returns (default: 100,000) from a normal distribution with mean μ and std σ.

Determine VaR values:

VaR(95%) = 5th percentile

VaR(99%) = 1st percentile

VaR(99.9%) = 0.1st percentile

Store values for visualization.

Output

Print summary metrics for each iteration

Plot VaR series over time for each confidence level

📊 Example Output
Printed Output: Mean, Std Dev, VaR(95%), VaR(99%), VaR(99.9%) per iteration.

Plot: Line chart showing VaR trends for:

95% Confidence

99% Confidence

99.9% Confidence
