# A Backtest A Day
Everyday I will be backtesting a different quant strategy for the markets

## Backtested Strategies

### Best Equal Weight Long Only Strategies

#### EW XS Long-Only Short-term Reversal
![image](https://github.com/replacementAI/A-Backtest-A-Day/assets/55959390/0b92dae3-c490-4b90-be12-49f116aa7a12)

| Description (Long Only)                  | Best Lookback (3 folds) | Sharpe |
|------------------------------------------|-------------------------|--------|
| [EW XS Long-Only Short-term Reversal][1] | 6 Days                  | 0.624  |
| [EW TS Long-Only Short-term Reversal][2] | 4 Days                  | 0.595  |
| [EW TS Long-Only Mean Reversion][3]      | 111 Days                | 0.582  |
| [EW XS Long-Only Pos Skew][4]            | 24 Days                 | 0.560  |
| [EW XS Long-Only Low Vol][5]             | 3 Days                  | 0.548  |
| [EW XS Long-Only Pos Kurtosis][6]        | 76 Days                 | 0.537  |
| [EW XS Long-Only Neg Skew][7]            | 107 Days                | 0.504  |
| [EW TS Long-Only Momentum][8]            | 188 Days                | 0.504  |
| [EW XS Long-Only Momentum][9]            | 124 Days                | 0.503  |

### Best Equal Weight Long/Short Strategies

#### EW XS L/S Short-term Reversal
![image](https://github.com/replacementAI/A-Backtest-A-Day/assets/55959390/64de2acd-6530-4f24-9ee3-c44c15f67e91)

| Description (Long Short)            | Best Lookback (3 folds) | Sharpe |
|-------------------------------------|-------------------------|--------|
| [EW XS L/S Short-term Reversal][10] | 6 Days                  | 0.688  |
| [EW TS L/S Short-term Reversal][11] | 4 Days                  | 0.522  |
| [EW XS L/S Pos Skew][12]            | 24 Days                 | 0.512  |
| [EW TS L/S Mean Reversion][13]      | 3 Days                  | 0.443  |
| [EW XS L/S Neg Kurt][14]            | 130 Days                | 0.384  |
| [EW XS L/S Neg Skew][15]            | 107 Days                | 0.355  |
| [EW XS L/S Pos Kurt][16]            | 4 Days                  | 0.288  |
| [EW XS L/S Momentum][17]            | 124 Days                | 0.211  |
| [EW TS L/S Momentum][18]            | 188 Days                | 0.181  |
| [EW XS L/S Low Vol][19]             | 17 Days                 | 0.103  |

### Best Ranked Long-Only Strategies

| Description (Long-only)        | Best Lookback (3 folds) | Sharpe |
|--------------------------------|-------------------------|--------|
| [RW XS Long-only Neg Skew][20] | 111 Days                | 0.572  |
| [RW XS Long-only Pos Kurt][21] | 5 Days                  | 0.524  |
| [RW XS Long-only Momentum][22] | 108 Days                | 0.444  |
| [RW TS Long-only Momentum][23] | 191 Days                | 0.439  |
| [RW XS Long-only Neg Kurt][24] | 51 Days                 | 0.433  |

## Methodology
The main metric I will be using to measure a strategy is the sharpe ratio. What is the sharpe ratio?
### Sharpe Ratio
The sharpe ratio is the average return of a strategy divided by its risk. Meaning if a strategy has high returns, and low risk, then it will have a high sharpe ratio. Why this metric and not total profit? Because total profit only keeps track of returns of a strategy, not risk, while sharpe ratio is calculated with both, allowing you to sleep better at night, instead of wondering if you are going to make 100% or lose 100% tomorrow.

### Other
First I will plot the cumulative return of each strategy over the entire sample, then I will the evaluate the sharpe of each strategy in a 3-fold cross validation to determine the best* parameters. The tickers used are the SPDR sector ETFs: XLE, XLU, XLB, XLK, XLI, XLV, XLF, XLP, and XLY. There are 3 reasons for using these groups of tickers:
1. Removes survivorship bias problem from using individual tickers
2. These ETFs were launched in 1998, giving a lot of data to work with.
3. Lastly, it is easier for an individual investor to attempt to replicate a strategy using just a few ETFs as opposed to having to a strategy using (for example) 500 stocks.

## Abbreviations
- TS = Time Series
- EW = Equal Weight
- L\S = Long Short
- XS = Cross Sectional
- Vol = Volatility
- Pos = Positive
- Neg = Negative
- Opp = Opposite
- RW = Rank Weight

## Credits
Code was provided by @quant_arb on Twitter, I added the cross-validation to try to better pick parameters.

[1]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20XS%20Long-Only%20Short-term%20Reversal.ipynb>
[2]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20TS%20Long-Only%20Short-term%20Reversal.ipynb>
[3]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20TS%20Long-Only%20Mean%20Reversion.ipynb>
[4]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20XS%20Long-Only%20Pos%20Skew.ipynb>
[5]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20XS%20Long-Only%20Low-Vol.ipynb>
[6]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20XS%20Long-Only%20Pos%20Kurt.ipynb>
[7]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20XS%20Long-Only%20Neg%20Skew.ipynb>
[8]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20TS%20Long-Only%20Momentum.ipynb>
[9]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20XS%20Long-Only%20Momentum.ipynb>

[10]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20XS%20L%5CS%20Short-term%20Reversal.ipynb>
[11]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20TS%20L%5CS%20Short-term%20Reversal.ipynb>
[12]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20XS%20L%5CS%20Pos%20Skew.ipynb>
[13]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20TS%20L%5CS%20Mean%20Reversion.ipynb>
[14]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20XS%20L%5CS%20Neg%20Kurt.ipynb>
[15]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20XS%20L%5CS%20Neg%20Skew.ipynb>
[16]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20XS%20L%5CS%20Pos%20Kurt.ipynb>
[17]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20XS%20L%5CS%20Momentum.ipynb>
[18]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20TS%20L%5CS%20Momentum.ipynb>
[19]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW-XS-L%5CS-Low-Vol.ipynb>

[20]: <>
[21]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/RW%20XS%20Long-Only%20Pos%20Kurtosis.ipynb>
[22]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/RW%20XS%20Long-only%20Momentum.ipynb>
[23]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/RW%20TS%20Long-Only%20Momentum.ipynb>
[24]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/RW%20XS%20Long-only%20Neg%20Kurt.ipynb>
