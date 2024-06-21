# Stateful Strategy Optimization
This README provides an overview of the stateful strategy optimization process, which uses Quantiacs libraries to implement and backtest a trading strategy with specific exit conditions. The strategy is optimized using multiple parameters to find the best performing combination.

## How to Run the Strategy
### In an Online Environment

The strategy can be executed in an online environment using Jupiter or JupiterLab on
the [Quantiacs personal dashboard](https://quantiacs.com/personalpage/homepage). To do this, clone the template in your
personal account.

### In a Local Environment

To run the strategy locally, you need to install the [Quantiacs Toolbox](https://github.com/quantiacs/toolbox).

## Strategy Overview

This strategy uses a stateful approach to manage long and short positions with specific exit conditions. It operates on NASDAQ-100 stocks and employs various indicators to make trading decisions.

### Key Features:
- **Universe:** NASDAQ-100 stocks
- **Trading Logic:** Positions are adjusted based on calculated signals, with conditional exits for taking profit, stopping loss, and day counting for short positions.
- **Indicators Used:** Simple Moving Average (SMA), Rate of Change (RoC), Average True Range (ATR), etc.
- **State Management:** Utilizes the Quantiacs state management system to maintain and update strategy state across different days.

### Strategy Components:
1. **Strategy Function:**
    - Define the strategy function which computes the weights (positions) based on signals and applies exit conditions.
    - The strategy adjusts weights according to the trading logic and exits conditions.
    - Conditional exits are applied to manage risks and capture profits.
2. **Data Loading and Preparation:**
    - Load stock data using qndata.stocks.load_ndx_data or another function for a different dataset.
3. **Optimize Strategy**
    - Run the optimization with defined parameter ranges.
4. **Analyze Results**
    - Extract and visualize the optimization results.
5. **Backtesting:**
    - Use the multipass backtester to evaluate the strategy performance over historical data.
    - Analyze the results and visualize performance metrics.

### Recommendations for Competitive Submissions:
- Limit the amount of exit functions to reduce computational demand.
- Limit the amount of parameters and use larger steps in ranges to avoid overfitting and reduce computational demand.
- Compare notebook statistics with the submission statistics to make sure there are no unintended interactions such as forward-looking.
