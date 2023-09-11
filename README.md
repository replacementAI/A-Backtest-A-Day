# A Backtest A Day
Everyday I will backtest a different quant strategy for the markets!

## Types of Strategies
- [Sector Rotation][1]
- [Precious Metals][2]
- [Agriculture Commodities][3]

## Best Long Only vs Long/Short Backtested Strategies

### Best [Sector Rotation][1] Strategies
#### [Best Long Only][4]
#### [Best Long Short][5]
![image](https://github.com/replacementAI/A-Backtest-A-Day/assets/55959390/c862d5c7-5f4c-4c13-a485-6873e37cb580)

### Best [Precious Metal][2] Strategies
#### [Best Long Only][6]
#### [Best Long Short][7]
![image](https://github.com/replacementAI/A-Backtest-A-Day/assets/55959390/ebc95a5a-a228-4beb-9b4f-6eaafcca9d5f)

### Best [Agriculture Commodity][3] Strategies
#### [Best Long Only][8]
#### [Best Long Short][9]
![image](https://github.com/replacementAI/A-Backtest-A-Day/assets/55959390/88afc716-5dde-47da-a185-491e962e0922)

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

[1]:<https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/README.md>
[2]:<https://github.com/replacementAI/A-Backtest-A-Day/tree/main/Metal/README.md>
[3]:<https://github.com/replacementAI/A-Backtest-A-Day/tree/main/Agriculture/README.md>
[4]:<https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/TS%20Long-Only%20STR.ipynb>
[5]:<https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/XS%20L%5CS%20STR.ipynb>
[6]:<https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Metal/TS%20Long-Only%20MOM.ipynb>
[7]:<https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Metal/XS%20L%5CS%20Low%20Skew.ipynb>
[8]:<>
[9]:<>
