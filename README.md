# Deep Hedging with Neural Networks under Black-Scholes and Heston Models

## Overview
This Jupyter notebook implements the concept of **Deep Hedging** as proposed in the paper:

> Buehler, Hans, et al. "Deep hedging." Quantitative Finance 19.8 (2019): 1271-1291.

The notebook compares traditional **Delta Hedging** under the **Black-Scholes Model** with **Neural Network-based Deep Hedging** strategies, incorporating considerations such as:
- Quadratic Loss (MSE)
- Conditional Value-at-Risk (CVaR) Loss
- Transaction Costs
- Heston Model (stochastic volatility)

## Contents
The notebook is organized as follows:

### 1. Black-Scholes Model (d=1)
1.1. Analytical price and delta computation using Black-Scholes formula
1.2. Monte Carlo simulation of underlying asset paths and option pricing
1.3. Profit and Loss (PnL) evaluation:
    - Without hedging
    - Delta hedging
1.4. Deep Hedging with Neural Networks (MSE loss)
1.5. Experiments with different NN architectures and hyperparameters:
    - Effect of normalization
    - Number of hidden layers
    - Hidden layer size
    - Activation functions
    - Single model vs different models for each timestep
    - CVaR loss
1.6. Deep Hedging with transaction costs

### 2. Heston Model (d=2)
2.1. Analytical price estimation via Monte Carlo simulation
2.2. Deep Hedging under Heston model with a 2-dimensional underlying (Price + Variance Swap)

## Key Features
- Monte Carlo Simulation for Black-Scholes and Heston Models
- Analytical Pricing Formula for Black-Scholes Options
- Delta Hedging and Deep Hedging PnL Comparison
- Neural Network Implementation using PyTorch
- Customizable Loss Functions (MSE, CVaR)
- Transaction Costs Modeling

## How to Run
1. Install the required libraries:
    ```bash
    pip install numpy scipy matplotlib seaborn torch tqdm
    ```
2. Open and execute the notebook cell by cell:
    ```bash
    jupyter notebook <notebook_name>.ipynb
    ```

## Dependencies
- Python 3.8+
- numpy
- scipy
- matplotlib
- seaborn
- torch
- tqdm

## Results
The notebook demonstrates that **Deep Hedging** can reduce hedging errors compared to classic delta hedging, especially under transaction costs and stochastic volatility (Heston Model).

Key observations:
- **Normalization** of asset prices is critical for stable training.
- **CVaR loss** improves tail risk performance compared to MSE.
- **Transaction costs** can be better handled using deep hedging than traditional delta hedging.

## File Structure
- `deep_hedging_experiments.ipynb`: Main Jupyter Notebook
- `requirements.txt`: Package dependencies (optional)

## License
This project is licensed under the **MIT License**. Feel free to use and adapt the code with proper attribution.

## Author
- [Your Name]
- [Your Contact Information / GitHub Profile]

## References
- Buehler, Hans, et al. "Deep hedging." Quantitative Finance 19.8 (2019): 1271-1291.
- https://arxiv.org/abs/1802.03042

