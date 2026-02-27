# Trader Performance vs Market Sentiment Analysis

## Objective

The goal of this project is to analyze how Bitcoin market sentiment (Fear/Greed Index) relates to trader behavior and performance on Hyperliquid. The analysis focuses on identifying patterns in profitability, trading activity, and risk across different sentiment conditions, and translating those patterns into practical strategy insights.

## Datasets Used

1) Bitcoin Market Sentiment (Fear/Greed Index)
    - Contains daily sentiment classification (Fear, Extreme Fear, Neutral, Greed, Extreme Greed).
    - Used to categorize each trading day by market sentiment.

2) Historical Trader Data (Hyperliquid)
    - Includes trade-level information such as account, execution price, trade size, side, timestamp, and closed PnL.

    - Used to compute performance and behavior metrics at daily and account levels.

Both datasets were aligned at the daily level to enable sentiment-based comparison.

## Methodology

The analysis was structured in three main stages:

1. Data Preparation
    - Loaded and inspected both datasets.

    - Checked for missing values and duplicates.

    - Converted timestamps to datetime format.

    - Aligned trades with daily sentiment data.

    - Simplified sentiment into three buckets: Fear, Neutral, and Greed.

2. Feature Engineering
    - Created key metrics for analysis:
    - Daily PnL per trader
    - Win rate (percentage of profitable trades)
    - Trade frequency per day
    - Volatility (standard deviation of daily PnL)
    - Activity-based trader segmentation (High vs Low activity)

3. Analysis
    - Compared average PnL across sentiment buckets.
    - Examined win rate differences.
    - Evaluated volatility and risk-adjusted performance.
    - Segmented traders by activity level to study behavioral differences.
    - Performed statistical tests (ANOVA) to validate observed differences.


## Key Insights
   - Traders are most active during Fear periods, suggesting higher market volatility.
   - Average daily PnL is higher during Fear, but volatility is also significantly higher.
   - Neutral periods show stronger risk-adjusted performance (higher mean-to-volatility ratio).
   - High-activity traders perform best during Fear conditions.
   - Low-activity traders perform relatively better during Greed conditions.
   - Overall statistical tests indicate that sentiment alone explains a small portion of performance variance, highlighting the importance of segmentation and risk management.

## Strategy Recommendations
1) Volatility-Aware Allocation During Fear
High-activity traders tend to perform better during Fear periods, likely due to increased volatility. During such periods, allocating more capital or flexibility to experienced traders may help capture short-term opportunities, while maintaining strict risk controls.

2) Structured Participation During Greed
Low-activity traders show stronger performance during Greed conditions. Trend-following strategies with moderate position sizing may be more effective during bullish sentiment phases.

Overall, a sentiment-aware and segment-aware allocation framework appears more appropriate than a uniform trading approach.


## How to Run
1) Clone the repository:
git clone https://github.com/Aaa-38/Trader_Sentiment_Analysis
cd trader_sentiment_analysis

2) Create a virtual environment:
python -m venv venv
venv\Scripts\activate

3) Install dependencies:
pip install -r requirements.txt

4) Open and run the notebook:
jupyter notebook

Run all cells in Trader_Sentiment_Analysis.ipynb to reproduce the analysis and results.