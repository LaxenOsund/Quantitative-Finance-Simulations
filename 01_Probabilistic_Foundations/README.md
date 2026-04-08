# 01: Probabilistic Foundations (Monty Hall Simulation)

## Project Overview
This project explores the relationship between theoretical probability and empirical results using a Large-Scale Monte Carlo simulation of the Monty Hall Paradox. 

The goal was to move beyond basic frequency analysis and apply rigorous statistical tests used in quantitative research to verify model accuracy.

## Key Statistical Concepts
* **Monte Carlo Methods:** Simulating 10,000,000 trials to estimate the true win-rate of the 'Switch' vs 'Stay' strategy.
* **Law of Large Numbers (LLN):** Visualizing the convergence of the win-rate as sample size increases, moving from high variance to stability.
* **Central Limit Theorem (CLT):** Running an "Average of Averages" experiment to observe the Normal Distribution (Bell Curve) of results.
* **Confidence Intervals:** Calculating a 95% Confidence Interval (CI) to quantify the margin of error in our simulation.

## Technical Implementation
* **Language:** Python
* **Libraries:** NumPy (Vectorized operations for speed), Matplotlib (Data Visualization)
* **Performance:** Utilized NumPy arrays to avoid slow Python loops, allowing for 10 million trials in sub-second time.

## Results
The simulation confirms a ~66.67% win rate for the switching strategy. The CLT analysis shows a clear Gaussian distribution centered at the theoretical mean, validating the robustness of the Monte Carlo model.