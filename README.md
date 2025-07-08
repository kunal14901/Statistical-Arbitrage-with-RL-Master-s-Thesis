# Advanced Statistical Arbitrage with Reinforcement Learning

## Project Overview
This repository contains my Master's thesis work on developing and benchmarking advanced statistical arbitrage strategies by integrating deep reinforcement learning with classical mean-reversion models. The project was conducted at the Indian Institute of Technology, Kharagpur under the guidance of Prof. Geetanjali Panda.

The objective was to construct dynamic, mean-reverting portfolios that adapt across varying market regimes while improving risk-adjusted returns compared to traditional approaches.

## Key Features

- **Hybrid Approach**: Combines classical statistical arbitrage techniques with modern deep reinforcement learning
- **Market Regime Adaptation**: Models dynamically adjust to volatile, trending, and sideways market conditions
- **Comprehensive Benchmarking**: Compares RL-based strategy against traditional Ornstein-Uhlenbeck and Distance Method approaches
- **Enhanced Performance**: Achieved superior returns with lower drawdowns through learned policy behavior

## Methodology

### Asset Selection
- Cointegration analysis to identify mean-reverting pairs
- Hurst exponent calculation to confirm mean-reversion properties
- Correlation analysis for pair selection

### Classical Strategies
1. **Ornstein-Uhlenbeck Process**: 
   - Models spread as mean-reverting stochastic process
   - Implements optimal thresholds based on process parameters

2. **Distance Method (z-score)**:
   - Traditional Bollinger-band like approach
   - Trades based on standardized spread deviations

### Reinforcement Learning Approach
- **Deep Q-Network (DQN) with LSTM layers**:
  - State space: Normalized spread values, technical indicators, market regime features
  - Action space: Entry/exit decisions and position sizing
  - Reward function: Risk-adjusted returns with penalties for drawdowns
- **Adaptive Policy Learning**:
  - Learns optimal trading rules without fixed thresholds
  - Adjusts to changing market conditions through experience replay

## Results (Out-of-Sample Backtest)

| Strategy          | Annual Return (%) | Sharpe Ratio | Max Drawdown (%) | Trades | Avg Holding (Days) |
|-------------------|------------------:|-------------:|-----------------:|-------:|-------------------:|
| OU Process        | 12.1              | 0.88         | 18.4             | 290    | ~4                 |
| Distance Method   | 10.6              | 0.79         | 20.1             | 250    | ~3                 |
| RL (DQN+LSTM)     | **19.8**          | **1.26**     | **11.7**         | 510    | ~2                 |

## Key Insights
- The RL-based model outperformed traditional methods by **63%** in annual returns
- Achieved **36% lower maximum drawdown** compared to classical approaches
- Demonstrated superior adaptability in non-stationary market environments
- More frequent trades with shorter holding periods captured mean-reversion opportunities more effectively

## Repository Structure
```
├── data/                   # Sample datasets and preprocessing scripts
├── classical_strategies/    # OU Process and Distance Method implementations
├── rl_model/               # DQN with LSTM implementation and training scripts
├── backtesting/            # Performance evaluation framework
├── results/                # Pre-computed results and visualizations
├── requirements.txt        # Python dependencies
└── thesis.pdf             # Complete thesis document
```

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/stat-arb-rl.git
   cd stat-arb-rl
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
1. Preprocess data:
   ```bash
   python data/preprocess.py
   ```

2. Run classical strategies:
   ```bash
   python classical_strategies/ou_process.py
   python classical_strategies/distance_method.py
   ```

3. Train RL model:
   ```bash
   python rl_model/train.py
   ```

4. Evaluate performance:
   ```bash
   python backtesting/compare_strategies.py
   ```

## Dependencies
- Python 3.8+
- NumPy, Pandas
- Scikit-learn, Statsmodels
- TensorFlow/Keras
- Matplotlib, Seaborn

## Future Work
- Incorporate additional market regime indicators
- Experiment with other RL algorithms (PPO, SAC)
- Extend to multi-asset portfolios
- Implement online learning for real-time adaptation

## Citation
If you find this work useful for your research, please consider citing:
```
[Your Thesis Citation Here]
```

## Contact
For questions or collaborations, please contact [iknir14901@gmail.com] or connect on [https://www.linkedin.com/in/kunal-kumar-9aa708200/].
