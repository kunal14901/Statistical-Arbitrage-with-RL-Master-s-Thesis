

````markdown
# 📉 Robust Glasso for High-Dimensional Portfolio Selection

Master's Thesis Project  
Indian Institute of Technology, Kharagpur  
Duration: Aug 2023 – Jan 2024  
Python Version: 3.8+  
License: MIT

---

## 🔍 Overview

This project implements a robust version of Graphical Lasso (Glasso) for portfolio optimization in high-dimensional financial datasets. The method enhances classical Glasso with robust statistics, making it resistant to outliers and better suited for volatile market conditions.

---

## 🚀 Key Features

- Robust covariance estimation using MCD and outlier-resistant techniques
- Sparse inverse covariance matrix using L1 regularization
- Handles large-scale asset universes (100–1000+ assets)
- GAN-enhanced alternative tested against Glasso variants
- Performance-tested under simulated crisis scenarios
- Visualization of asset networks and risk clustering

---

## 📦 Installation

```bash
git clone https://github.com/yourusername/robust-glasso-portfolio.git
cd robust-glasso-portfolio
pip install -r requirements.txt
````

---

## 🛠️ Usage

```python
from robust_glasso import RobustGraphicalLasso
from portfolio_optimizer import MeanVarianceOptimizer

# Initialize robust glasso
rg = RobustGraphicalLasso(alpha=0.01, robust_threshold=2.5)

# Fit on returns data (assets x observations)
rg.fit(returns_data)

# Get robust precision matrix
precision_matrix = rg.get_precision()

# Optimize portfolio
optimizer = MeanVarianceOptimizer(precision_matrix)
weights = optimizer.maximize_sharpe()
```

---

## 📊 Results

| Metric           | Traditional Glasso | Robust Glasso |
| ---------------- | ------------------ | ------------- |
| Sharpe Ratio     | 1.2                | 1.5           |
| Max Drawdown     | -25%               | -18%          |
| Out-of-sample R² | 0.65               | 0.78          |

---

## 📚 Documentation

Complete methodology, mathematical formulations, and testing results are detailed in the thesis report (not publicly available).

---

## 🔗 Related Work

Also see the companion Master's Thesis:
[📊 Statistical Arbitrage with Deep Reinforcement Learning](https://github.com/yourusername/stat-arb-rl)
Adaptive mean-reversion strategies using LSTM-based DQN models under dynamic market regimes.

---

## 🤝 Contributing

Academic collaborations and feedback are welcome through IIT Kharagpur institutional channels.

---

## 📫 Contact

Kunal Kumar
Final Year | Mathematics & Computing | IIT Kharagpur
Email: [iknir1234@gmail.com](mailto:iknir1234@gmail.com)
LinkedIn: [https://www.linkedin.com/in/kunal-kumar-9aa708200/](https://www.linkedin.com/in/kunal-kumar-9aa708200/)

---

## 📜 License

This project is licensed under the MIT License.
Note: Research content is part of academic work submitted to IIT Kharagpur and remains confidential.

```
```
