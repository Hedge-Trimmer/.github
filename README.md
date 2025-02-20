# Hedge Trimmer

*Cutting Through Market Noise with Precision*

Hedge Trimmer is an advanced algorithmic trading platform designed to automate and optimize trading decisions using a diverse suite of quantitative strategies. Our flagship product integrates seamlessly with the Alpaca API for live (and paper) trading, enabling both simulated and real-time execution of sophisticated trading algorithms.

---

## Overview

Hedge Trimmer combines rigorous quantitative research with state-of-the-art technology to empower traders with:
- **Robust Automated Trading:** Execute trades based on real-time signals derived from multiple technical and macroeconomic indicators.
- **Ensemble Strategy:** Leverage an ensemble of trading strategies—including moving average crossovers, momentum analysis, and macro indicator integration—to generate optimized BUY/SELL/HOLD signals.
- **Adaptive Risk Management:** Implement stop loss, take profit, and trailing stop logic to protect capital while capturing market opportunities.
- **Modular Design:** Easily swap or modify strategies with a well-organized codebase, ensuring quick adaptation to evolving market conditions.

---

## Key Features

- **Live Trading Loop:**  
  Continuously polls market data and generates signals for a predefined list of symbols, triggering simulated or live orders via the Alpaca API.

- **Advanced Signal Generation:**  
  Utilizes a variety of strategies (e.g., moving average crossover, RSI, EMA, Bollinger Bands, momentum, machine learning models like LSTM and XGBoost, and a custom ensemble strategy) to create reliable trading signals.

- **Simulated Portfolio:**  
  In addition to live trading, Hedge Trimmer supports a simulated portfolio for backtesting and risk-free strategy evaluation without transaction costs.

- **Dynamic Strategy Weighting:**  
  Our flagship ensemble strategy dynamically adjusts weights based on market regimes (bullish, bearish, or sideways) using macro indicators like SPY and VIX.

- **Caching & API Integration:**  
  Efficient data retrieval and caching mechanisms ensure minimal downtime and reduced API calls when fetching historical market data.

---

## Technology Stack

- **Programming Languages:** Python  
- **Core Libraries:**  
  - `pandas`, `numpy` for data manipulation  
  - `alpaca_trade_api` for trading connectivity  
  - Machine Learning: `tensorflow` (for LSTM), `xgboost`  
- **Other Tools:**  
  - `pickle` for local caching of market data  
  - `optree` for strategy parameter management (if needed)
- **Deployment:**  
  Runs on local servers or can be deployed to cloud environments supporting Python.

---

## Code Structure

The repository is structured into two main modules:

### `main.py`
- **Live Trading Loop:**  
  Continuously polls market data for a list of symbols, retrieves real-time pricing, and invokes the signal generator.
- **Order Execution:**  
  Contains functions to simulate trades (via a simulated portfolio account) as well as to submit live orders using the Alpaca API.
- **Risk Management:**  
  Implements exit conditions such as stop loss, take profit, and trailing stop based on dynamic market conditions.

### `algo.py`
- **Strategy Implementations:**  
  Provides a collection of trading strategies, including:
  - Technical strategies (e.g., moving average crossover, RSI, EMA, Bollinger Bands)
  - Machine Learning strategies (e.g., LSTM and XGBoost)
  - Custom strategies (e.g., VWAP, momentum, TWAP, mean reversion)
  - An **ensemble strategy** that combines multiple indicators, dynamically weighting signals based on market regime.
- **Macro Indicator Integration:**  
  Uses additional market data (SPY, VIX) to guide the ensemble strategy for enhanced signal accuracy.

---

## Contact
For more information about Hedge Trimmer or to get in touch:

- LinkedIn: HedgeTrimmer

