# Quant-Research-Project---Shubhankar-Mondal

# Quant Research Assignment

We wanted to provide an example of what solving problems as an intern at True Beacon would look like. Below is an excerpt from a strategy our team is actively researching and deploying in financial markets. We have defined the key concepts required for this assignment below. The goal of the assignment is to learn about your statistical acumen and applied modelling capabilities. N**o other understanding of markets or any underlying financial concepts is required.**  

**Glossary**

- **Nifty**: Equity Index representing 50 of the largest and most liquid stocks listed on the National Stock Exchange of India (NSE)
- **Bank Nifty**: Equity Index on the NSE comprising the most liquid and large-capitalized Indian banking stocks.
- **Option:** a contract that helps you take a view of the direction and volatility of an underlying stock/index.
    - **Time To Expiry:** refers to the duration from the current date to the expiry date of the option contract.
- **Index Options:**  instruments that allow investors to trade the overall movement of indices like Nifty and Bank Nifty.
- **Pairs Trading**: involves simultaneously buying and shorting two correlated stocks when their prices diverge. The strategy profits from the pair's price ratio returning to its historical norm, aiming to capitalize on relative price movements.
    - **Volatility Pair Trading:** type of pairs trading strategy that involves taking advantage of the difference in volatility between two correlated securities. The strategy assumes that the volatility will either return to or move away from the historical mean.
- **Implied Volatility (IV)**: metric that reflects the market’s expectation of future volatility of the underlying asset or index price.

**Research Thesis**

Nifty and Bank Nifty indices have significant overlap in terms of their constituents and weights. Our thesis is that their volatilities are also likely to be affected by similar market conditions and macroeconomic factors. We can thus construct a pairs trading strategy that attempts to capture any dispersion that may occur between the volatilities of the two indices

This assignment will involve building a pairs trading strategy to test this hypothesis. The output we are looking for is a medium-frequency strategy that has a trading horizon ranging between 30 min to 5 days. 

**Dataset**

[data.parquet](https://prod-files-secure.s3.us-west-2.amazonaws.com/f3d54618-4ee1-480d-b8f7-25c361e2c7b2/12d14740-f5b4-4ce9-9d4d-b9d0b3cd5548/data.parquet)

1. Time series of minute-level implied volatilities (IVs) of Bank Nifty and Nifty.
2. Time To Expiry (TTE) for the series.
3. Indian market trading hours are between 09:15 and 15:30. 
4. There may be some missing values in the dataset.
5. The formula to calculate P/L has been specified below. If you modify your IV or spread series, make sure you modify the P/L equation as well.

**Deliverables**

1. Build a [z-score based](https://en.wikipedia.org/wiki/Standard_score) trading system. It would use the z-scores of the spread to identify when volatility has diverged away from the historical mean and act accordingly. The calculation of the P/L here constitutes the base model.
2. Build a better model than the z-score trading system. Be creative in the modelling techniques you implement.
3. Compare your proposed model with the base model with the goal of optimizing the absolute P/L, Sharpe Ratio, and Drawdown of your strategy.
