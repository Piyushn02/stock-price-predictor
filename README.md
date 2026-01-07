# Stock Price Prediction via Monte Carlo Simulation

A quantitative finance project utilizing Geometric Brownian Motion (GBM) to forecast future stock prices for **Allianz SE (ALV.DE)**. This model generates thousands of potential price paths to provide a probabilistic assessment of risk and return.

## Key Features

* **Stochastic Modeling:** Implements GBM ($dS_t = \mu S_t dt + \sigma S_t dW_t$) to simulate random price walks.
* **Automated Data:** Fetches real-time historical data via the `yfinance` API.
* **Risk Metrics:** Calculates Drift and Volatility parameters from historical log returns.
* **Confidence Intervals:** Projects 68% (1 Sigma) and 95% (2 Sigma) confidence ranges for future prices.
* **Visualization:** Plots simulated price trajectories over a 252-day horizon.

## Methodology

The simulation derives **Drift** (expected return) and **Volatility** (standard deviation) from historical data (Jan 2000 – Present). Future prices are projected using the discrete GBM formula:

$$P_t = P_{t-1} \cdot e^{(\text{drift} + \sigma \cdot Z)}$$

*Where $Z$ is a random variable following a standard normal distribution.*

<img width="1262" height="773" alt="image" src="https://github.com/user-attachments/assets/489f29ba-88d5-4912-9324-a5b57bf9e717" />

Best and Worst Cases

Worst Simulation $/share: 119.1

Average Simulation $/share: 412.04

BestSimulation $/share: 1361.85

Confidence Intervals
1 Sigma (1 S.D.): 68% confident that price after 252 days will fall between: €275.52 and €548.57

2 Sigma (2 S.D.): 95% confident that price after 252 days will fall between: €138.99 and €685.1


