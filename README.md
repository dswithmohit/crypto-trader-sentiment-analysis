Crypto Trader Behavior vs Market Sentiment

This project analyzes how crypto trader performance and behavior change under different market sentiment conditions using the Fear & Greed Index.

The goal is to understand whether market psychology affects trader profitability, leverage usage, and trading activity.

Objective
Compare trader profitability on Fear vs Greed days
Identify behavioral changes in trading patterns
Segment traders by leverage, frequency, and consistency
Evaluate whether market sentiment influences trading outcomes
Dataset
Trader Execution Data

Contains trade-level information including:

trader account
execution price
trade size
trade direction
realized PnL
timestamp

Total trades analyzed: 211,224

Market Sentiment Data

Daily Fear & Greed Index classifications:

Extreme Fear
Fear
Neutral
Greed
Extreme Greed
Methodology
Data Cleaning
Standardized column names
Converted timestamps
Filtered closed trades
Feature Engineering
Daily trader PnL
Win rate
Trade frequency
Average trade size
Long/short ratio
Sentiment Merge
Aggregated trader metrics per trader per day
Merged with daily sentiment classification
Key Visualizations
Performance Distribution: Fear vs Greed profitability
Behavior Comparison: trade frequency, leverage, and position bias
Trader Segmentation: sentiment impact across trader types

Charts are saved in:

outputs:
Key Insights
Trader PnL varies across market sentiment regimes
Trading activity increases during Fear periods
High-frequency traders dominate profitability
Market sentiment provides useful context for trading behavior analysis
Tech Stack
Python
Pandas
NumPy
Matplotlib
Seaborn
Jupyter Notebook
