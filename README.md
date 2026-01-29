# Cross-Sectional Data Analysis - Cryptocurrency Market

## Objective
Using Python with Pandas to explore cross-sectional momentum in Cryptocurrencies. 
An analysis first approach is used. 

"Backtesting while researching is like drinking and driving. 
Do not research under the influence of a backtest." - Marcos López de Prado (2018)

*Translation: Backtest results can bias your research. Analyze features first, backtest later.*

## Key-Findings 
- Cross-sectional momentum exists in Cryptocurrencies
- Short leg unprofitable (works only as a hedge during bear markets)
- Long-only variant shows high drawdowns without regime filter 
- Regime filter improves performance but may be too restrictive 
- Long-only with regime variant is profitable and outperforms the cross-sectional baseline 

## Methodolgy
- Universe selection based on trading volume 
- Explorative data analysis
- Bootstrapping for difference in conditioal expecteded returns (feature selection)
- **Regime Filter**: Cumsum based, with monthly recalculation
- Features:
  - Momentum for 7, 20 and 30 days
  - Momentum divergence (Score from two momentum features)
  - Price to moving average ratio
  - Normalized opening price
- Features are transformed into z-scores
- Cross-sectional binning

## Limitations
While performances of strategys are in a simple manner evaluated, several aspects are necessary for a complete framework.
- A complete backtest with transaction costs and slippage. Both aspects or the complete backtest are not present.
- Out-of-sample performance 
- Monte Carlo Simulations with Geometric Brownian Motion for stress-tests/permutations (performance from the final strategy compared to randomness)
- Other regime classifications like Hidden Markov Models
- Non linear methods or machine learning methods are not demonstrated

## Future Improvements
This was my first complete cross-sectional data analysis. I am more than guilty for curve-fitting in terms of cumulative returns performance. 
Before this notebook existed, several other notebooks, with other rules and other features was backtested up and down. 

Here are my improvements for next analytical projects:
- Set a clear research goal
- Define a set of features in advance
- Clean documentation in a notebook research 
- Using models like linear regression or logistic regression
- Modularization if needed
- First research, than backtesting 

### Final words
A backtest in Python is fast implemented and I thought it was something like magic, to see, how the performance on historical data looked.
But one aspect was missing: Understanding. With understanding not only the strategy is meant, also if and how a feature does provide some value.
Defining features and test several rules directly in a backtest did not helped me. Yes, maybe one feature with a different lookback period made the backtest look good.
But why should a feature add some value? Why should a combination of features add value or increase the expected conditional return? It is not possible to get this answer from a backtest.
This is why I decided to go the data analytics way and put the quote from Marcos López de Prado on the top. 
I hope you found this notebook informative and interesting.

### Disclaimer
This research notebook is provided for educational and analytical demonstration purposes only.



