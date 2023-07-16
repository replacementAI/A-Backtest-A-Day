# A Backtest A Day
Everyday I will be backtesting a different quant strategy for the markets

## Top Backtested Strategies
| Description                     | Sharpe (avg 3 fold) |
|---------------------------------|---------------------|
| EW TS Long-Only Trend Following | 0.5819755958600765  |
| EW TS Long-Only Momentum        | 0.5040385748680951  |
|                                 |                     |

## Methodology
First I will calculate the sharpe of each strategy over the entire sample, then I will the evaluate performance of each strategy in a 3-fold cross validation to determine the best* parameters.

## Abbreviations
- TS = Time Series
- EW = Equal Weight
- LS = Long Short
- XS = Cross Sectional

## Credits
Code was provided by @quant_arb on Twitter, I added the cross-validation part to try to better pick parameters.
