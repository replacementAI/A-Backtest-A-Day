# A Backtest A Day
Everyday I will be backtesting a different quant strategy for the markets

## Top Backtested Strategies
| Description                              | Sharpe (avg 3 fold) |
|------------------------------------------|---------------------|
| [EW XS Long-Only Short-term Reversal][1] | 0.6243479755318527  |
| [EW TS Long-Only Trend Following][2]     | 0.5819755958600765  |
| [EW TS Long-Only Momentum][3]            | 0.5040385748680951  |
| [EW XS Long-Only Momentum][4]            | 0.5025833917716915  |

## Methodology
First I will calculate the sharpe of each strategy over the entire sample, then I will the evaluate performance of each strategy in a 3-fold cross validation to determine the best* parameters.

## Abbreviations
- TS = Time Series
- EW = Equal Weight
- LS = Long Short
- XS = Cross Sectional

## Credits
Code was provided by @quant_arb on Twitter, I added the cross-validation to try to better pick parameters.

[1]:
[2]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20TS%20Long-Only%20Trend%20Following.ipynb>
[3]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20TS%20Long-Only%20Momentum.ipynb>
[4]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20XS%20Long-Only%20Momentum.ipynb>
