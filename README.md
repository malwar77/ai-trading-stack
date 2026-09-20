# 8 GitHub Repos for Building an AI Trading Stack

A curated collection of foundational open-source repositories for building autonomous, algorithmic, and AI-driven quantitative trading systems.

---

## The AI Trading Stack Architecture

A production-grade autonomous trading pipeline follows this modular pipeline:

```
Market Data  ──>  Strategy Engine  ──>  Backtesting  ──>  Risk Controls  ──>  Execution  ──>  Autonomous Agents
```

> **Note**: Treat these tools as quantitative research foundations and engineering infrastructure, not out-of-the-box profit systems. Test extensively with paper trading and historical simulation before live deployment.

---

## Repositories

### 1. Multi-Agent Decision Systems
* **[virattt/ai-hedge-fund](https://github.com/virattt/ai-hedge-fund)**
  * **Role:** Multi-agent decision framework
  * **Summary:** Simulates a collaborative investment committee where specialized agents (fundamental, technical, valuation, sentiment, risk manager) evaluate trades and debate conclusions before sizing and execution.

### 2. Strategy Development & Automated Crypto Bots
* **[freqtrade/freqtrade](https://github.com/freqtrade/freqtrade)**
  * **Role:** Crypto trading bot framework
  * **Summary:** Battle-tested open-source cryptocurrency algorithmic trading bot featuring backtesting, hyperparameter optimization, machine learning integration (FreqAI), telegram control, and automated execution.

### 3. Exchange Connectivity & Infrastructure
* **[ccxt/ccxt](https://github.com/ccxt/ccxt)**
  * **Role:** Unified crypto exchange API
  * **Summary:** Universal multi-language library connecting to over 100 cryptocurrency exchanges and prediction markets with consistent interfaces for public market data and private account/order management.

### 4. High-Performance Event-Driven Engines
* **[nautechsystems/nautilus_trader](https://github.com/nautechsystems/nautilus_trader)**
  * **Role:** Production-grade event-driven backtesting and live trading engine
  * **Summary:** High-performance, Rust-native, event-driven trading platform supporting multi-asset, multi-venue execution, highly accurate tick-level backtesting, and low-latency production operation.

### 5. Market Making & Liquidity Provision
* **[hummingbot/hummingbot](https://github.com/hummingbot/hummingbot)**
  * **Role:** Market making & arbitrage automation
  * **Summary:** Open-source platform tailored for building, configuring, and running automated market making (AMM), cross-exchange market making, and arbitrage strategies across centralized and decentralized exchanges.

### 6. Autonomous Agents & On-Chain Interaction
* **[elizaOS/eliza](https://github.com/elizaOS/eliza)**
  * **Role:** Autonomous agent operating system
  * **Summary:** Framework for developing autonomous AI agents capable of maintaining state, reasoning, interacting across social channels (Discord, X, Telegram), and managing crypto wallets for on-chain transactions.

### 7. Reinforcement Learning for Finance
* **[AI4Finance-Foundation/FinRL](https://github.com/AI4Finance-Foundation/FinRL)**
  * **Role:** Deep reinforcement learning trading framework
  * **Summary:** Educational and research platform connecting financial environments to modern deep RL algorithms (PPO, DDPG, SAC) with standardized data pipelines for algorithmic portfolio management.

### 8. Python Algorithmic Frameworks
* **[jesse-ai/jesse](https://github.com/jesse-ai/jesse)**
  * **Role:** Strategy development & backtesting
  * **Summary:** Advanced Python-based cryptocurrency algorithmic trading framework designed for fast strategy prototyping, realistic backtesting, and clean code architecture.
