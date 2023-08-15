# A Backtest A Day
Everyday I will backtest a different quant strategy for the markets!

## Types of Strategies
- [Sector Rotation][1]
- [Precious Metals][2]

## Best Backtested Strategies

### Best Time Series Long/Short Strategy
#### Short-term Reversal [code][3]
![image](https://github.com/replacementAI/A-Backtest-A-Day/assets/55959390/dcc697d1-ab34-4d98-87a2-488d0dff2104)

### Best Cross Sectional Long/Short Strategy
#### Short-term Reversal [code][4]
![image](https://github.com/replacementAI/A-Backtest-A-Day/assets/55959390/c817fa61-c873-401b-8d9d-4f8c94960eb0)

## Methodology
The main metric I will be using to measure a strategy is the sharpe ratio. What is the sharpe ratio?
### Sharpe Ratio
The sharpe ratio is the average return of a strategy divided by its risk. Meaning if a strategy has high returns, and low risk, then it will have a high sharpe ratio. Why this metric and not total profit? Because total profit only keeps track of returns of a strategy, not risk, while sharpe ratio is calculated with both, allowing you to sleep better at night, instead of wondering if you are going to make 100% or lose 100% tomorrow.
### How to use strategy yourself
1. Either download the notebook or copy the code into a Python script
2. Remove the end date parameter from yf.download()
3. Print the last row of ```weighted_signal``` using ```print(weighted_signal.iloc[-1])``` (I will update the notebooks to already have this)
4. Go long the positive weights and (if the strategy is L/S,) short the negative weights
### Other
First I will the evaluate the sharpe of each lookback of a strategy in a 5-fold cross validation to determine the best* parameters, then I will plot the cumulative return of the lookback with the highest sharpe.
These backtests DO NOT take fees/slippage into account, in my opinion this isnt a problem for the long-only strategies, but needs to be considered for long/short strategies.

## Abbreviations
- TS = Time Series
- L\S = Long Short
- XS = Cross Sectional
- Vol = Volatility
- MOM = Momentum
- STR = Short-term Reversal

## Credits
Code was provided by @quant_arb on Twitter, I added the cross-validation to try to better pick parameters.

[1]:<https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector>
[2]:<https://github.com/replacementAI/A-Backtest-A-Day/tree/main/Metal>
[3]:<https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/TS%20L%5CS%20STR.ipynb>
[4]:<https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/XS%20L%5CS%20STR.ipynb>
