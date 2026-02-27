# Trader Performance vs Market Sentiment — Summary Report

## Objective

This project analyzes the relationship between Bitcoin market sentiment (Fear/Greed Index) and trader behavior on Hyperliquid. The goal is to determine whether sentiment conditions influence trading performance and whether sentiment-aware strategy adjustments can improve outcomes.

## Methodology
The analysis was conducted in three structured phases:

1) Data Preparation
    - Loaded and validated both datasets.
    - Converted timestamps to datetime format.
    - Aligned trade-level data with daily sentiment.
    - Simplified sentiment into three buckets: Fear, Neutral, and Greed.

2) Feature Engineering
    - Computed daily PnL per trader.
    - Calculated win rate (percentage of profitable trades).
    - Measured trade frequency per day.
    - Evaluated volatility (standard deviation of daily PnL).
    - Segmented traders into High-Activity and Low-Activity groups based on trade count.

3) Performance & Risk Analysis
    - Compared average PnL across sentiment conditions.
    - Evaluated win rates by sentiment.
    - Measured volatility and simple risk-adjusted performance.
    - Conducted ANOVA tests to assess statistical significance.
    - Analyzed performance differences across trader segments.

## Key Findings
- Trading activity increases significantly during Fear periods.
- Average daily PnL is highest during Fear, but volatility is also highest.
- eutral periods exhibit the strongest risk-adjusted performance (higher return per unit volatility).
- High-activity traders perform best during Fear conditions.
- Low-activity traders perform relatively better during Greed conditions.
- Statistical tests indicate that sentiment alone explains a small proportion of overall PnL variance, suggesting that segmentation and risk management play a larger role.

## Strategy Recommendations

1) Volatility-Based Allocation During Fear
High-activity traders appear better suited to volatile environments. During Fear periods, allocating greater flexibility or capital to experienced traders may improve performance, provided risk controls remain strict.

2) Trend-Focused Participation During Greed
Low-activity traders perform relatively better during Greed conditions. Structured trend-following strategies with moderate position sizing may be more effective in these environments.

Overall, a sentiment-aware and segment-aware allocation approach appears more appropriate than a uniform trading strategy.

## Conclusion
While sentiment alone does not strongly determine performance outcomes, it correlates with meaningful shifts in trader behavior and volatility regimes. Incorporating both sentiment and trader segmentation into strategic decision-making can potentially improve capital efficiency and risk-adjusted returns.