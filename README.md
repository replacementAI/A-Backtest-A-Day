# A Backtest A Day
Everyday I will be backtesting a different quant strategy for the markets

## Top Backtested Strategies

### EW XS Long-Only Short-term Reversal
![image](https://github.com/replacementAI/A-Backtest-A-Day/assets/55959390/0b92dae3-c490-4b90-be12-49f116aa7a12)

| Description                              | Sharpe (avg 3 fold) |
|------------------------------------------|---------------------|
| [EW XS Long-Only Short-term Reversal][1] | 0.6243479755318527  |
| [EW TS Long-Only Short-term Reversal][2] | 0.5948150993839677  |
| [EW TS Long-Only Trend Following][3]     | 0.5819755958600765  |
| [EW XS Long-Only Pos Skew][4]            | 0.5595241995242272  |
| [EW XS Long-Only Low Vol][5]             | 0.5484778491819274  |
| [EW XS Long-Only Pos Kurtosis][6]        | 0.5371160392292454  |
| [EW XS Long-Only Neg Skew][7]            | 0.5043078891599437  |
| [EW TS Long-Only Momentum][8]            | 0.5040385748680951  |
| [EW XS Long-Only Momentum][9]            | 0.5025833917716915  |

## Methodology
First I will calculate the sharpe of each strategy over the entire sample, then I will the evaluate performance of each strategy in a 3-fold cross validation to determine the best* parameters. The tickers used are the SPDR sector ETFs: XLE, XLU, XLB, XLK, XLI, XLV, XLF, XLP, and XLY. There are 3 reasons for using these groups of tickers: 1. Removes survivorship bias problem from using individual tickers 2. These ETFs were launched in 1998, giving a lot of data to work with. 3. Lastly, it is easier for an individual investor to attempt to replicate a strategy using just a few ETFs as opposed to having to a strategy using (for example) 500 stocks.

## Abbreviations
- TS = Time Series
- EW = Equal Weight
- LS = Long Short
- XS = Cross Sectional
- Vol = Volatility
- Pos = Positive
- Neg = Negative

## Credits
Code was provided by @quant_arb on Twitter, I added the cross-validation to try to better pick parameters.

[1]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20XS%20Long-Only%20Short-term%20Reversal.ipynb>
[2]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20TS%20Long-Only%20Short-term%20Reversal.ipynb>
[3]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20TS%20Long-Only%20Trend%20Following.ipynb>
[4]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20XS%20Long-Only%20Pos%20Skew.ipynb>
[5]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20XS%20Long-Only%20Low-Vol.ipynb>
[6]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20XS%20Long-Only%20Pos%20Kurt.ipynb>
[7]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20XS%20Long-Only%20Neg%20Skew.ipynb>
[8]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20TS%20Long-Only%20Momentum.ipynb>
[9]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/EW%20XS%20Long-Only%20Momentum.ipynb>
