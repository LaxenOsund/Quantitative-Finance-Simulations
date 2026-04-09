# 03: Algorithmic Backtesting (SMA Crossover Strategy)

## Project Overview
This project involves the development of a systematic trend-following backtester. Unlike the previous stochastic simulations, this model utilizes 26 years of historical market data (2000–2026) to evaluate the efficacy of a Simple Moving Average (SMA) crossover strategy.

The primary objective was to determine if a rules-based entry/exit system could outperform a passive "Buy & Hold" approach in terms of absolute return and risk mitigation.

## Strategy Logic: The "Golden Cross"
The algorithm monitors two primary signals:
* **Fast Signal (50-Day SMA):** Represents short-term price momentum.
* **Slow Signal (200-Day SMA):** Represents the long-term market trend.

**Rules:**
1. **Enter Long:** When the 50-day SMA crosses above the 200-day SMA.
2. **Exit to Cash:** When the 50-day SMA crosses below the 200-day SMA.

## Key Quantitative Concepts
* **Vectorized Backtesting:** Leveraged NumPy and Pandas for high-speed computation of signals and returns across 6,500+ trading days.
* **Look-ahead Bias Prevention:** Implemented a one-day shift on signals to ensure trades are executed at the next available opening price, reflecting realistic trading conditions.
* **Maximum Drawdown (MDD):** Analyzed the "Peak-to-Trough" decline to quantify the emotional and financial "pain" of the strategy.
* **Risk-Adjusted Return (Sharpe Ratio):** Evaluated whether the excess return justified the volatility taken by the strategy.

## Performance Analysis (2000–2026)

| Metric | Buy & Hold (SPY) | SMA Crossover Strategy |
| :--- | :--- | :--- |
| **Total Return** | ~640% | **~651%** |
| **Max Drawdown** | -55.19% | **-33.72%** |
| **Annulized (CAGR)** | 7.93% | **8.00%** |
| **Sharpe Ratio** | Lower | **Higher** |

## Conclusion
While the total returns between the two approaches were comparable over the long horizon, the SMA strategy proved superior in **Capital Preservation**. By exiting the market during the 2008 Financial Crisis and the 2022 Bear Market, the strategy reduced the maximum loss by nearly **22%**. 

For a quantitative investor, this higher Sharpe Ratio represents a more efficient use of capital and a significantly more sustainable investment "ride."