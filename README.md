# Dynamic-Portfolio-using-reinforcement-learning

Deep Reinforcement Learning for Stock Trading: Portfolio Allocation

Team Members

Mohammed Yasir Khattib (Reg. No: 2348043)

Nishant Rodrigues (Reg. No: 2348045)

Jilson Rosario (Reg. No: 2348033)

Overview

This project aims to design and implement an automated trading solution for portfolio allocation using Deep Reinforcement Learning (DRL). The stock trading process is modeled as a Markov Decision Process (MDP), and the trading strategy is optimized to maximize portfolio returns.

Project Structure

1. Problem Definition

The stock trading task is framed as a Reinforcement Learning problem with:

State: Observations derived from historical and technical stock data.

Action: Portfolio weight allocations for stocks.

Reward: Change in portfolio value due to executed actions.

Environment: Simulated trading environment using real market data.

2. Getting Started

2.1 Install Packages

Install required dependencies using the FinRL library and additional packages:

pip install git+https://github.com/AI4Finance-LLC/FinRL-Library.git
pip install exchange_calendars pyfolio stockstats
pip install finrl[full]

2.2 Create Necessary Folders

To ensure smooth execution, create the following folders:

data_save_dir

trained_model_dir

tensorboard_log_dir

results_dir

2.3 Import Packages

Core packages include:

pandas, numpy, matplotlib

FinRL modules

stable-baselines3

Yahoo Finance API

3. Data Preparation

3.1 Data Source

Data is obtained from Yahoo Finance API for Dow 30 stocks.

Features include Open, High, Low, Close, and Volume.

Additional technical indicators (e.g., MACD, RSI) and covariance matrices are calculated.

3.2 Preprocessing Steps

Handle missing data.

Engineer features such as MACD, RSI, and covariance matrices.

Normalize data for the model.

4. Environment Design

The trading environment is implemented based on OpenAI Gym. It simulates live market conditions for portfolio allocation with real market data.

Key components:

State Space: Stock prices, technical indicators, and covariance matrices.

Action Space: Portfolio weights for each stock.

Reward Function: Portfolio return after executing an action.

5. Deep Reinforcement Learning Models

Implemented DRL algorithms for training the trading agent include:

PPO (Proximal Policy Optimization)

A2C (Advantage Actor-Critic)

DDPG (Deep Deterministic Policy Gradient)

The agent interacts with the environment, updates its policy, and learns to optimize portfolio allocation.

6. Backtesting and Evaluation

After training, the model's performance is evaluated through:

BacktestStats: Calculates key performance metrics.

BacktestPlot: Visualizes portfolio performance over time.

Baseline Comparison: Compares the agent's performance with standard indices (e.g., S&P 500).

Results and Insights

The DRL-based trading agent demonstrated a significant improvement in portfolio returns compared to a baseline strategy.

The use of technical indicators and covariance matrices enhanced the agent's ability to manage risk and maximize returns.

Backtesting highlighted the robustness of the model during volatile market periods.

Future Work

Incorporate additional DRL algorithms (e.g., SAC, TD3).

Extend the environment to multi-asset trading scenarios.

Enhance risk management by integrating dynamic hedging techniques.

Develop a GUI for real-time trading and visualization.

How to Run

Clone the repository.

Install the necessary dependencies.

Prepare the dataset using the scripts in the data folder.

Train the model using the provided Jupyter notebooks or Python scripts.

Backtest and evaluate the model performance.

Acknowledgments

FinRL Library: For providing a robust foundation for financial reinforcement learning.

Yahoo Finance API: For historical stock data.

For any inquiries or feedback, please contact the team members.

