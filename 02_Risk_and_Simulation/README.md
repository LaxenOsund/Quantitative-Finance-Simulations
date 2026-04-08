# 02: Risk & Wealth Simulation (Monte Carlo Growth)

## Project Overview
This project models long-term wealth accumulation using stochastic simulation. Unlike linear projections, this model accounts for market volatility and the "path-dependency" of investment returns.

## Key Financial Concepts
* **Log-Normal Distribution:** Utilized Geometric Brownian Motion principles to ensure asset prices remain non-negative and reflect realistic market behavior.
* **Volatility Drag:** Adjusted the expected return ($\mu - 0.5\sigma^2$) to account for the geometric mean's tendency to lag the arithmetic mean in volatile environments.
* **Sequence of Returns Risk:** Demonstrated how the timing of market downturns affects portfolio solvency, visualized through 50% and 90% probability bands.

## Technical Features
* **Dynamic Configuration:** Implemented a centralized `CONFIG` system for easy parameter stress-testing (adjusting sigma, contributions, or time horizons).
* **Advanced Visualization:** High-contrast shaded confidence bands to represent risk zones rather than individual chaotic paths.
* **Success Probability:** A binary success/fail metric against a fixed retirement goal of $2.5M.

## Analysis
The model reveals that even with a positive average return, high volatility can significantly widen the 5th and 95th percentile outcomes. This highlights the importance of risk-adjusted planning over simple average-return forecasting.