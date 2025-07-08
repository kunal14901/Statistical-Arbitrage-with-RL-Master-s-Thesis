Here's the direct content for your `README.md` file:

```markdown
# Advanced Statistical Arbitrage with Reinforcement Learning

## 📌 Overview
Master's thesis project developing adaptive statistical arbitrage strategies by combining:
- Classical mean-reversion models (Ornstein-Uhlenbeck, Distance Method)
- Deep Reinforcement Learning (DQN with LSTM)
- Market regime detection

**Key Innovation:** RL agent that dynamically adjusts trading policies across volatile/trending/sideways markets.

## 🚀 Performance Highlights (Out-of-Sample)
| Strategy          | Return (%) | Sharpe | Max DD (%) |
|-------------------|-----------:|-------:|-----------:|
| OU Process        | 12.1       | 0.88   | 18.4       |
| Distance Method   | 10.6       | 0.79   | 20.1       |
| **RL (DQN+LSTM)** | **19.8**   | **1.26** | **11.7** |

## 🛠️ Implementation
### Asset Selection
```python
# Cointegration test
from statsmodels.tsa.stattools import coint
score, pvalue, _ = coint(asset1, asset2)
```

### RL Framework
```python
# DQN-LSTM Architecture
model = Sequential([
    LSTM(64, input_shape=(lookback, n_features)),
    Dense(32, activation='relu'),
    Dense(n_actions)
])
```

## 📂 Repository Structure
```
├── data/            # Historical price data
├── notebooks/       # Jupyter notebooks for analysis
│   ├── 1_pair_selection.ipynb
│   ├── 2_classical_strategies.ipynb
│   └── 3_rl_training.ipynb
├── src/
│   ├── classical/   # OU and Distance Method
│   └── rl/          # DQN implementation
└── results/         # Backtest reports
```

## ⚙️ Setup
1. Clone repo:
   ```bash
   git clone https://github.com/yourusername/stat-arb-rl.git
   cd stat-arb-rl
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## 🏎️ Quick Start
```bash
# Run classical strategies
python src/classical/ou_process.py --pair AAPL_MSFT

# Train RL agent
python src/rl/train.py --lookback 30 --episodes 1000
```

## 📊 Sample Results
![Equity Curve](results/equity_curve.png)

## 📜 Citation
```bibtex
@mastersthesis{yourthesis2025,
  title={Advanced Statistical Arbitrage with RL},
  author={Your Name},
  year={2025},
  school={IIT Kharagpur}
}
```

## 📬 Contact
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)]([your-linkedin](https://www.linkedin.com/in/kunal-kumar-9aa708200/))
[![Email](https://img.shields.io/badge/Email-Contact-red)](iknir1234@email.com)
```
