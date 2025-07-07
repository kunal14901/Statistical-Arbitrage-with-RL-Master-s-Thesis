Here's a well-structured `README.md` for your project, summarizing your work on statistical arbitrage strategies with deep reinforcement learning:

```markdown
# Statistical Arbitrage with Deep Reinforcement Learning

**Master's Thesis Project**  
*Indian Institute of Technology, Kharagpur*  
*Advisor: Prof. Geetanjali Panda*  
*Oct 2024 - Feb 2025*

## 📌 Overview
This project develops **adaptive statistical arbitrage strategies** by integrating deep reinforcement learning (RL) with classical mean-reversion models. The goal is to construct dynamic portfolios that outperform traditional approaches in varying market regimes (trending, volatile, sideways) while minimizing drawdowns.

## 🔍 Methodology
### Pair Selection
- Identified optimal asset pairs using:
  - **Cointegration tests** (ADF, Johansen)
  - **Hurst exponent** for mean-reversion tendency
  - Correlation analysis

### Classical Strategies (Benchmark)
1. **Ornstein-Uhlenbeck (OU) Process**: 
   - Mean-reversion trading based on OU parameters (θ, μ, σ)
2. **Distance Method (Z-score)**:
   - Threshold-based entry/exit using normalized price spread

### RL-Based Strategy (Proposed)
- **Deep Q-Network (DQN) with LSTM**:
  - State space: Normalized spreads, volatility, regime indicators
  - Actions: Entry/exit/sizing in continuous space
  - Reward: Risk-adjusted returns (Sharpe ratio focus)
  - Trained on multiple market regimes for adaptability

## 📊 Key Results (Out-of-Sample Backtest)
| Strategy          | Annual Return | Sharpe Ratio | Max Drawdown | Trades | Avg Holding Days |
|-------------------|--------------|--------------|--------------|--------|------------------|
| OU Process        | 12.1%        | 0.88         | 18.4%        | 290    | ~4               |
| Distance Method   | 10.6%        | 0.79         | 20.1%        | 250    | ~3               |
| **RL (DQN+LSTM)** | **19.8%**    | **1.26**     | **11.7%**    | 510    | ~2               |

**Insight**: The RL model achieved **63% higher returns** and **36% lower drawdowns** vs. classical methods by learning adaptive policies.

## 🛠️ Technical Implementation
- **Languages**: Python
- **Libraries**: 
  - PyTorch (DQN+LSTM implementation)
  - Statsmodels (cointegration tests)
  - Pandas/Numpy (data processing)
  - Backtrader (strategy backtesting)


## 🧮 Skills Demonstrated
- Statistical Arbitrage · Time Series Analysis · Reinforcement Learning
- Python · PyTorch · Trading Strategy Development

*Note: Code and proprietary data are not publicly shared per university guidelines.*
```

### Key Features:
1. **Clear Hierarchy**: Separates problem, methods, results, and implementation.
2. **Benchmark Comparison**: Highlights RL's outperformance in a table.
3. **Technical Depth**: Mentions specific tests (ADF/Johansen) and RL architecture.
4. **Modular Structure**: Shows how the project is organized.
5. **Concise Metrics**: Focuses on the most compelling numbers (63% better returns).
