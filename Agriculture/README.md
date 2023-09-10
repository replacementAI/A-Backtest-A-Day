# Agriculture ETF Strategies

## Backtested Strategies

### Best Time Series Long Only Strategies

| Strat | Sharpe |
|-------|--------|
| [STR][1]   | 0.693  |
| [MOM][2]   | 0.065  |

![image](https://github.com/replacementAI/A-Backtest-A-Day/assets/55959390/b0024e0f-6d63-40dd-97db-3c19acd53fad)

### Best Time Series Long/Short Strategies

| Strat | Sharpe |
|-------|--------|
| [MOM][3]   | 0.444  |
| [STR][4]   | 0.359  |

![image](https://github.com/replacementAI/A-Backtest-A-Day/assets/55959390/c83a9562-0798-44c2-a81e-564e31ace65b)

### Best Cross Sectional Long-Only Strategies

| Strat           | Sharpe |
|-----------------|--------|
| [STR][5]        | 0.681  |
| [Low Kurt][6]   | 0.223  |
| [Low Vol][7]    | 0.124  |
| [Low Skew][8]   | 0.077  |
| [High Kurt][9]  | 0.043  |
| [High Skew][10] | 0.028  |
| [MOM][11]       | -0.037 |

![image](https://github.com/replacementAI/A-Backtest-A-Day/assets/55959390/244a42a6-fbea-4b44-95f9-4b8b9942eb54)

### Best Cross Sectional Long/Short Strategies

| Strat           | Sharpe |
|-----------------|--------|
| [STR][12]       | 1.53   |
| [Low Kurt][13]  | 0.586  |
| [Low Vol][14]   | 0.494  |
| [Low Skew][15]  | 0.454  |
| [High Kurt][16] | 0.208  |
| [High Skew][17] | 0.163  |
| [MOM][18]       | 0.073  |

![image](https://github.com/replacementAI/A-Backtest-A-Day/assets/55959390/bebc2b6f-837e-4dcb-88cf-81813b3db22b)

## Methodology
The measured metric is the sharpe ratio.
### How to use strategy yourself
1. Either download the notebook or copy the code into a Python script
2. Remove the end date parameter from yf.download()
3. Print the last row of ```weighted_signal``` using ```print(weighted_signal.iloc[-1])``` (I will update the notebooks to already have this)
4. Go long the positive weights and (if the strategy is L/S,) short the negative weights
### Other
I will the evaluate the sharpe of each lookback of a strategy in a 5-fold cross validation to determine the best* parameters. The tickers used are these ETFs: GLD, SLV, PPLT, and PALL. I use ETFs because its an easy to use asset an individual investor to attempt to replicate a strategy with.
### Correlations of each asset
![image](https://github.com/replacementAI/A-Backtest-A-Day/assets/55959390/def50a65-cdd8-472b-bdd6-81a2497d9953)

## Abbreviations
- TS = Time Series
- L\S = Long Short
- XS = Cross Sectional
- Vol = Volatility
- MOM = Momentum
- STR = Short-term Reversal

## Credits
Code was provided by @quant_arb on Twitter, I added the cross-validation to try to better pick parameters.

[1]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Agriculture/TS%20Long-Only%20STR.ipynb>
[2]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Agriculture/TS%20Long-Only%20MOM.ipynb>
[3]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Metal/TS%20L%5CS%20MOM.ipynb>
[4]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Metal/TS%20L%5CS%20STR.ipynb>
[5]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Metal/XS%20Long-Only%20Low%20Skew.ipynb>
[6]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Metal/XS%20Long-Only%20Low%20Kurt.ipynb>
[7]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Metal/XS%20Long-Only%20High%20Kurt.ipynb>
[8]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Metal/XS%20Long-Only%20MOM.ipynb>
[9]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Metal/XS%20Long-Only%20High%20Skew.ipynb>
[10]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Metal/XS%20Long-Only%20STR.ipynb>
[11]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Metal/XS%20Long-Only%20Low-Vol.ipynb>
[12]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Metal/XS%20L%5CS%20Low%20Skew.ipynb>
[13]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Metal/XS%20L%5CS%20MOM.ipynb>
[14]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Metal/XS%20L%5CS%20High%20Kurt.ipynb>
[15]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Metal/XS%20L%5CS%20Low%20Kurt.ipynb>
[16]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Metal/XS%20L%5CS%20High%20Skew.ipynb>
[17]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Metal/XS%20L%5CS%20STR.ipynb>
[18]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Metal/XS%20L%5CS%20Low-Vol.ipynb>
