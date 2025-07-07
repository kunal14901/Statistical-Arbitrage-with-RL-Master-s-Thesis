```markdown
# 📊 Statistical Arbitrage with Deep Reinforcement Learning

**🎓 Master's Thesis Project**  
*Indian Institute of Technology, Kharagpur*  
**Advisor**: Prof. Geetanjali Panda  
**Duration**: Oct 2024 – Feb 2025  

---

## 📌 Overview

This research explores **adaptive statistical arbitrage** by integrating **deep reinforcement learning (DRL)** with classical mean-reversion strategies. The objective is to construct dynamic trading strategies that adjust to changing market regimes—trending, volatile, and sideways—while improving returns and reducing drawdowns.

---

## 🔬 Methodology

### 🧠 Pair Selection
- **Cointegration Tests**: Augmented Dickey-Fuller (ADF), Johansen Test  
- **Mean-Reversion Detection**: Hurst Exponent  
- **Correlation Filtering**: Top correlated pairs selected from NIFTY50 constituents  

### 🧮 Classical Benchmarks
1. **Ornstein-Uhlenbeck Process**  
   - Trade signals generated from deviations from long-term mean
2. **Z-Score Distance Method**  
   - Enter/exit based on standardized spread thresholds

### 🤖 RL-Based Strategy (Proposed)
- **Model**: Deep Q-Network (DQN) with LSTM  
- **State Space**: Spread features, volatility, rolling z-scores, market regime labels  
- **Actions**: Enter long/short, hold, exit, position sizing  
- **Reward Function**: Risk-adjusted return (Sharpe-optimized)  
- **Training Regimes**: Simulated episodes across trending, volatile, and mean-reverting phases  

---

## 📊 Results (Out-of-Sample Backtest)

| Strategy            | Annual Return | Sharpe Ratio | Max Drawdown | Trades |  Avg Holding Period |
|---------------------|---------------|--------------|--------------|--------|---------------------|
| Ornstein-Uhlenbeck  | 12.1%         | 0.88         | 18.4%        | 290    | ~4 Days             |
| Z-Score Distance    | 10.6%         | 0.79         | 20.1%        | 250    | ~3 Days             |
| RL (DQN + LSTM)     | **19.8%**     | 1.26         | 11.7%**      | 510    | ~2 Days             |

> 📈 **Insight**: The RL-based model outperformed classical methods by **+63% in returns** and **–36% in drawdown**, thanks to its ability to learn from and adapt to changing market conditions.

---

## 🛠️ Technical Stack

- **Languages**: Python  
- **Libraries**:  
  - `PyTorch` – DQN & LSTM implementation  
  - `Statsmodels` – Statistical tests (ADF, Johansen)  
  - `Backtrader` – Custom backtesting engine  
  - `Pandas`, `NumPy` – Data preprocessing and feature engineering  

---

## 🧠 Key Skills Demonstrated

- Quantitative Research · Statistical Arbitrage · Time Series Modeling  
- Reinforcement Learning · Market Regime Classification · Deep Learning (LSTM-DQN)  
- Python · PyTorch · Backtesting & Risk Metrics  

---


---

## 🔐 Disclaimer

> *Note: Source code and proprietary data are not publicly shared due to academic and institutional restrictions. For demonstration purposes only.*

---

## 📫 Contact

**Kunal Kumar**  
Final Year | Mathematics & Computing, IIT Kharagpur  
📧 [iknir14901@gmail.com]  
🔗 [https://www.linkedin.com/in/kunal-kumar-9aa708200/]

---

## 📜 License

This project is licensed under the **MIT License**.

