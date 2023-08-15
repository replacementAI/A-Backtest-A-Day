# Metal ETF Strategies

## Backtested Strategies

### Best Time Series Long Only Strategies

| Strat | Sharpe |
|-------|--------|
| [MOM][1]   | 0.615  |
| [STR][2]   | 0.480  |

### Best Time Series Long/Short Strategies

| Strat | Sharpe |
|-------|--------|
| [MOM][3]   | 0.444  |
| [STR][4]   | 0.359  |

### Best Cross Sectional Long-Only Strategies

| Strat          | Sharpe |
|----------------|--------|
| [Low Skew][5]  | 0.508  |
| [Low Kurt][6]  | 0.460  |
| [High Kurt][7] | 0.371  |
| [MOM][8]       | 0.357  |
| [High Skew][9] | 0.286  |
| [STR][10]      | 0.249  |
| [Low-Vol][11]  | 0.212  |

### Best Cross Sectional Long/Short Strategies

| Strat           | Sharpe |
|-----------------|--------|
| [Low Skew][12]  | 0.658  |
| [MOM][13]       | 0.522  |
| [High Kurt][14] | 0.514  |
| [Low Kurt][15]  | 0.223  |
| [High Skew][16] | 0.187  |
| [STR][17]       | 0.166  |
| [Low-Vol][18]   | -0.089 |

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

[1]:
[2]:
[3]:
[4]:
[5]:
[6]:
[7]:
[8]:
[9]:
[10]:
[11]:
[12]:
[13]:
[14]:
[15]:
[16]:
[17]:
[18]:
