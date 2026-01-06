# Stock Price Prediction via Monte Carlo Simulation 📈

A quantitative finance project that forecasts the future stock price of **Allianz SE (ALV.DE)** and other assets using **Monte Carlo Simulations** based on Geometric Brownian Motion (GBM).

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat-square)
![Finance](https://img.shields.io/badge/Finance-Quantitative-green?style=flat-square)
![Status](https://img.shields.io/badge/Status-Educational-orange?style=flat-square)

## 📖 Overview

Predicting stock prices is notoriously difficult due to market volatility. This project avoids simple linear regression in favor of a stochastic approach. By modeling thousands of potential future price paths, it provides a probabilistic assessment of risk and return rather than a single price target.

The core algorithm uses **Geometric Brownian Motion (GBM)**, the standard mathematical model for asset prices in continuous time.

## ⚡ Key Features

* **Real-Time Data Integration:** Automatically fetches historical data using the `yfinance` API.
* **Stochastic Modeling:** Implements the GBM formula ($dS_t = \mu S_t dt + \sigma S_t dW_t$) to simulate random walks.
* **Risk Analysis:** Calculates **Drift** and **Volatility** from historical log returns.
* **Confidence Intervals:** Outputs 68% (1 Sigma) and 95% (2 Sigma) confidence intervals to define the probable range of future prices.
* **Visualization:** Plots simulated price trajectories over a 250-day (1 trading year) horizon.

## 🛠️ Technologies

* **Python**
* **Pandas & NumPy** (Vectorized calculations and data manipulation)
* **Matplotlib** (Data visualization)
* **SciPy** (Statistical distribution functions)
* **YFinance** (Market data retrieval)

## 🚀 Installation & Usage

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/yourusername/stock-prediction-monte-carlo.git](https://github.com/yourusername/stock-prediction-monte-carlo.git)
    cd stock-prediction-monte-carlo
    ```

2.  **Install dependencies**
    ```bash
    pip install numpy pandas yfinance matplotlib scipy
    ```

3.  **Run the Simulation**
    Open the Jupyter Notebook and run all cells:
    ```bash
    jupyter notebook "allianz price prediction.ipynb"
    ```

## 📊 Methodology

The simulation is built on two primary components derived from historical data (starting from Jan 2000):

1.  **Drift ($\mu - \frac{1}{2}\sigma^2$):** The expected long-term return of the stock, adjusted for variance drag.
2.  **Volatility ($\sigma$):** The standard deviation of daily log returns.

The model generates future prices using the formula:
$$P_t = P_{t-1} \cdot e^{(\text{drift} + \sigma \cdot Z)}$$
*Where $Z$ is a random variable following a standard normal distribution.*

## 📉 Sample Results

*Note: Due to the random nature of Monte Carlo simulations, results vary with every run.*

**Simulation Target:** Allianz SE (ALV.DE)
* **Forecast Horizon:** 252 Days
* **1 Sigma Range (68% Probability):** Price likely falls between **€X** and **€Y**.
* **2 Sigma Range (95% Probability):** Price likely falls between **€A** and **€B**.


Contributions are welcome! Please feel free to submit a Pull Request.
