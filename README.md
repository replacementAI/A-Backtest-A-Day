# A Backtest A Day
Everyday I will backtest a different quant strategy for the markets!

## Backtested Strategies

### Best Time Series Long Only Strategy

### Best Time Series Long/Short Strategy

### Best Cross Sectional Long-Only Strategy

### Best Cross Sectional Long/Short Strategy

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

## Abbreviations
- TS = Time Series
- L\S = Long Short
- XS = Cross Sectional
- Vol = Volatility
- MOM = Momentum
- STR = Short-term Reversal

## Credits
Code was provided by @quant_arb on Twitter, I added the cross-validation to try to better pick parameters.
