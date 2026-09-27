# Risk-Parity-Investment-Strategy
3-Asset Risk Parity Allocation Execution Engine in Python


A 0-to-1 systematic trading framework built in Python, combining inverse-volatility Risk Parity allocation (SPY, GLD, BNO), dynamic backtesting, institutional risk metrics, and automated REST API order execution via Alpaca.

# Strategy & Performance Metrics (1-Year Backtest)

| Metric | Risk Parity Strategy (SPY/GLD/BNO) | 100% SPY Benchmark |

| **Annualized Return** | **29.36%** | 18.08% |
| **Annualized Volatility** | **12.69%** | 12.99% |
| **Sharpe Ratio (Rf = 5.18%)** | **1.90** | 0.99 |
| **Sortino Ratio (Downside)** | **2.55** | 1.53 |
| **Max Drawdown (Peak-to-Trough)**| -9.82% | **-8.88%** |
| **1-Day 95% VaR** | **1.20%** | 1.27% |

# Architecture Features
1. **Dynamic Risk Parity Engine**: Rebalances portfolio capital inversely to 30-day annualized rolling volatility ($w_i \propto 1/\sigma_i$).
2. **REST API Execution**: Integrated with Alpaca SDK for whole-share calculation, buying power guardrails, and automated trade routing.
3. **Institutional Risk Tear Sheet**: Dynamically pulls live 10-Year Treasury Yields (`^TNX`) to measure real-time Sharpe/Sortino performance.
