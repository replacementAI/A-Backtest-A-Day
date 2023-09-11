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
| [STR][3]   | 1.844  |
| [MOM][4]   | 0.362  |

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

![image](https://github.com/replacementAI/A-Backtest-A-Day/assets/55959390/56e87a5f-4a84-4167-b13a-8e45cc662799)

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

![image](https://github.com/replacementAI/A-Backtest-A-Day/assets/55959390/bb2dfc47-968f-493d-9aaa-a5d47af7fd36)


## Methodology
The measured metric is the sharpe ratio.
### How to use strategy yourself
1. Either download the notebook or copy the code into a Python script
2. Remove the end date parameter from yf.download()
3. Print the last row of ```weighted_signal``` using ```print(weighted_signal.iloc[-1])``` (I will update the notebooks to already have this)
4. Go long the positive weights and (if the strategy is L/S,) short the negative weights
### Other
I will the evaluate the sharpe of each lookback of a strategy in a 5-fold cross validation to determine the best* parameters. The tickers used are these ETFs: WEAT, CORN, SOYB, and CANE. I use ETFs because its an easy to use asset an individual investor to attempt to replicate a strategy with.
### Correlations of each asset
![image](https://github.com/replacementAI/A-Backtest-A-Day/assets/55959390/31e4da58-8ddc-46cf-bc42-32f9423a17e5)


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

[3]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Agriculture/TS%20L%5CS%20STR.ipynb>
[4]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Agriculture/TS%20L%5CS%20MOM.ipynb>

[5]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Agriculture/XS%20Long-Only%20STR.ipynb>
[6]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Agriculture/XS%20Long-Only%20Low%20Kurt.ipynb>
[7]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Agriculture/XS%20Long-Only%20Low-Vol.ipynb>
[8]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Agriculture/XS%20Long-Only%20Low%20Skew.ipynb>
[9]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Agriculture/XS%20Long-Only%20High%20Kurt.ipynb>
[10]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Agriculture/XS%20Long-Only%20High%20Skew.ipynb>
[11]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Agriculture/XS%20Long-Only%20MOM.ipynb>

[12]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Agriculture/XS%20L%5CS%20STR.ipynb>
[13]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Agriculture/XS%20L%5CS%20Low%20Kurt.ipynb>
[14]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Agriculture/XS%20L%5CS%20Low-Vol.ipynb>
[15]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Agriculture/XS%20L%5CS%20Low%20Skew.ipynb>
[16]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Agriculture/XS%20L%5CS%20High%20Kurt.ipynb>
[17]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Agriculture/XS%20L%5CS%20High%20Skew.ipynb>
[18]: <https://github.com/replacementAI/A-Backtest-A-Day/blob/main/Agriculture/XS%20L%5CS%20MOM.ipynb>
