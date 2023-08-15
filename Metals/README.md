# Metal ETF Strategies

## Backtested Strategies

### Best Time Series Long Only Strategies

| Strat | Sharpe |
|-------|--------|
| [STR][1]   | 0.599  |
| [MOM][2]   | 0.369  |

### Best Time Series Long/Short Strategies

| Strat | Sharpe |
|-------|--------|
| [STR][3]   | 0.515  |
| [MOM][4]   | 0.238  |

### Best Cross Sectional Long-Only Strategies

| Strat     | Sharpe |
|-----------|--------|
| [STR][5]       | 0.601  |
| [Low Skew][6]  | 0.553  |
| [High Skew][7] | 0.504  |
| [Low Vol][8]   | 0.498  |
| [High Kurt][9] | 0.495  |
| [Low Kurt][10]  | 0.393  |
| [MOM][11]       | 0.369  |

### Best Cross Sectional Long/Short Strategies

| Strat     | Sharpe |
|-----------|--------|
| [STR][12]       | 0.697  |
| [Low Skew][13]  | 0.415  |
| [High Skew][14] | 0.375  |
| [High Kurt][15] | 0.282  |
| [Low Vol][16]   | 0.093  |
| [Low Kurt][17]  | 0.074  |
| [MOM][18]       | 0.016  |

## Methodology
The measured metric is the sharpe ratio.
### How to use strategy yourself
1. Either download the notebook or copy the code into a Python script
2. Remove the end date parameter from yf.download()
3. Print the last row of ```weighted_signal``` using ```print(weighted_signal.iloc[-1])``` (I will update the notebooks to already have this)
4. Go long the positive weights and (if the strategy is L/S,) short the negative weights
### Other
I will the evaluate the sharpe of each lookback of a strategy in a 5-fold cross validation to determine the best* parameters. The tickers used are the SPDR sector ETFs: XLE, XLU, XLB, XLK, XLI, XLV, XLF, XLP, and XLY. There are 3 reasons for using these groups of tickers:
1. Removes survivorship bias problem from using individual tickers
2. These ETFs were launched in 1998, giving a lot of data to work with.
3. Lastly, it is easier for an individual investor to attempt to replicate a strategy using just a few ETFs as opposed to having to a strategy using (for example) 500 stocks.
### Correlations of each asset
![image](https://github.com/replacementAI/A-Backtest-A-Day/assets/55959390/585a19d0-b4d2-41c8-95e9-8d9d723f791e)

## Abbreviations
- TS = Time Series
- L\S = Long Short
- XS = Cross Sectional
- Vol = Volatility
- MOM = Momentum
- STR = Short-term Reversal

## Credits
Code was provided by @quant_arb on Twitter, I added the cross-validation to try to better pick parameters.

[1]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/TS%20Long-Only%20STR.ipynb>
[2]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/TS%20Long-Only%20MOM.ipynb>
[3]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/TS%20L%5CS%20STR.ipynb>
[4]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/TS%20L%5CS%20MOM.ipynb>
[5]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/XS%20Long-Only%20STR.ipynb>
[6]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/XS%20Long-Only%20Low%20Skew.ipynb>
[7]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/XS%20Long-Only%20High%20Skew.ipynb>
[8]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/XS%20Long-Only%20Low-Vol.ipynb>
[9]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/XS%20Long-Only%20High%20Kurtosis.ipynb>
[10]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/XS%20Long-Only%20Low%20Kurtosis.ipynb>
[11]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/XS%20Long-Only%20MOM.ipynb>
[12]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/XS%20L%5CS%20STR.ipynb>
[13]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/XS%20L%5CS%20Low%20Skew.ipynb>
[14]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/XS%20L%5CS%20High%20Skew.ipynb>
[15]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/XS%20L%5CS%20High%20Kurtosis.ipynb>
[16]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/XS%20L%5CS%20Low-Vol.ipynb>
[17]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/XS%20L%5CS%20Low%20Kurtosis.ipynb>
[18]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Sector/XS%20L%5CS%20MOM.ipynb>
