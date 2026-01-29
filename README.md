# Cross-Sectional Data Analysis - Cryptocurrency Market

## Objective
Using Python with Pandas to explore cross-sectional Momentum in Cryptocurrencys. 
An analysis first approach is used. 

"Backtesting while researching is like drinking and driving. 
Do not research under the influence of a backtest." - Marcos López de Prado (2018)

## Key-Findings 
- Cross-sectional momentum exists in Cryptocurrencys
- Shorting Spot is not directly possible
- Long-only variant requires a regime filter
- Without regime filter a futures hedging strategy is neccessary
- Long-only with regime variant is profitable and outperforms the cross-sectional baseline 

## Methodolgy
- Universe selection based on trading volume 
- Explorative data analysis
- Bootstrapping for difference in conditioal expecteded returns (feature selection)
- Features:
-- Momentum for 7, 20 and 30 days
-- Momentum divergence (Score from two momentum features)
-- Moving average to price ratio
-- Normalized opening price
- Features are transformed into z-scores
- Cross-sectional binning


