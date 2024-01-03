# Quantitative_trading_EUR_USD
A quantitative trading backtesting system conducts backtesting on specified financial market data. This project will focus on the market of the EUR/USD exchange rate.

Backtest Report
Strategy Overview:

- This backtest evaluates three different trading strategies: `SmaCross`, `TripleCross`, and `RSICross`. Each strategy is implemented using the Backtrader framework, focusing on moving average crossovers and RSI (Relative Strength Index) signals.


## 1.`SmaCross Strategy`

Parameters:

- Longer-term Moving Average Period (n1): 885

- Shorter-term Moving Average Period (n2): 244

Strategy Logic:

- Golden Cross: A bullish signal where the shorter-term moving average crosses above the longer-term moving average.

- Death Cross: A bearish signal where the shorter-term moving average crosses below the longer-term moving average.

Results:
- Best Parameters: 
 n1 = 885, 
 n2 = 244, size = 10000000, 
Sharpe Ratio = 0.461163

#### Trading Logic:

- Execute a buy if the shorter-term moving average crosses above the longer-term moving average.

- Execute a sell if the shorter-term moving average crosses below the longer-term moving average.
Only long positions, no short positions.


## 2. `TripleCross Strategy`
Parameters:

- First Moving Average Period (n1): 548

- Second Moving Average Period (n2): 206

- Third Moving Average Period (n3): 118

Strategy Logic:
- Execute a buy signal if both the shorter-term and middle moving averages cross above the longer-term moving average.

- Execute a sell signal if both the shorter-term and middle moving averages cross below the longer-term moving average.

Results:
- Best Parameters: n1 = 548, n2 = 206, n3 = 118, return = 67.2%, Sharpe Ratio = 1.07

- Window Ratio: Approximately 55:21:13

## 3. `RSICross Strategy`
Parameters:

- Upper Bound for RSI (upper_bound): 70

- Lower Bound for RSI (lower_bound): 30

- RSI Calculation Window (rsi_window): 130

Strategy Logic:

- Execute a buy if the RSI crosses above the upper bound.

- Execute a sell if the RSI crosses below the lower bound.

Results:
- Best Parameters: upper_bound = 70, lower_bound = 30, rsi_window = 133, return = 47, Sharpe Ratio = 0.87

Conclusion:

- Each strategy has shown promising results based on the provided parameters and backtesting environment. 

- The TripleCross strategy, with a return of 67.2% and a sharp ratio of 1.07, demonstrates strong performance. However, it's important to note that backtesting results might not guarantee future performance, and market conditions should be considered before implementing any strategy in live trading. 

- Adjustments to parameters and additional risk management techniques could further enhance the strategies' robustness.
