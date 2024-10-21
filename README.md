# Portfolio Optimization: Resampled Efficient Frontier

This project uses Markowitz' variance-covariance method to optimize asset allocation. In particular, we integrate Michaud's resampling efficient frontier to maximize the risk-return of the portfolio. 

This portfolio optimization technique was developed by Richard Michaud to address the limitations of the traditional mean-variance optimization approach. The method aims to create more stable and robust portfolios by incorporating statistical resampling techniques to account for the inherent uncertainty and estimation errors in the inputs (expected returns, variances, and covariances).

Simulating Multiple Scenarios:
Michaud's approach begins by generating multiple simulations of the input data (expected returns, variances, and covariances). These are created by randomly sampling from the estimated distributions of the asset returns. This process is akin to performing a Monte Carlo simulation.

Optimizing for Each Scenario:
For each simulated set of inputs, the traditional mean-variance optimization is performed to generate an efficient frontier. This yields multiple efficient frontiers based on different sets of simulated data.

Averaging the Efficient Frontiers:
The individual efficient frontiers obtained from each scenario are then averaged (or "resampled") to create the resampled efficient frontier. This averaging process smooths out the extreme portfolio weights that arise from using the original, single-set optimization, providing a more stable and realistic representation of optimal portfolios.

Constructing the Resampled Portfolio:
For a given risk level, the portfolio on the resampled efficient frontier is obtained by averaging the portfolio weights across the different optimized portfolios from the simulations.
This results in portfolios that are less sensitive to the original input estimation errors and are expected to perform better out-of-sample (i.e., in real market conditions).
