Crypto Trader Behavior vs Market Sentiment

This project analyzes how crypto trader performance and behavior change under different market sentiment conditions (Fear vs Greed).

The analysis combines trader execution data with the Crypto Fear & Greed Index to understand whether trader profitability, leverage usage, and trading behavior vary depending on market psychology.

Objective

The goal of this analysis is to answer the following questions:

Do traders perform better during Greed or Fear market conditions?
Does trader behavior change when sentiment shifts?
Which types of traders are most affected by sentiment?
Can sentiment signals be used to improve trading risk management?
📂 Project Structure
crypto-trader-sentiment-analysis
│
├── data
│   ├── raw                # Original datasets
│   └── processed          # Cleaned datasets
│
├── notebooks
│   └── trader_sentiment_analysis.ipynb
│
├── outputs                # Charts and analysis outputs
│
├── src
│   └── data_processing.py # Data cleaning utilities
│
├── README.md
├── requirements.txt
└── .gitignore
 Dataset
Trader Execution Data

Contains individual trade records including:

trader account
coin traded
execution price
trade size
trade direction
realized PnL
timestamp

Total trades analyzed: 211,224

Closed trades used for analysis: 104,408

Market Sentiment Data

Source: Crypto Fear & Greed Index

Each day is classified as:

Extreme Fear
Fear
Neutral
Greed
Extreme Greed
⚙️ Methodology

The analysis pipeline includes:

 Data Cleaning
Standardize column names
Convert timestamps
Filter closed trades
Extract trading date
 Feature Engineering

Derived features include:

daily trader PnL
win rate
trade frequency
leverage proxy
long/short bias
 Sentiment Integration

Trader activity was aggregated per trader per day and merged with the daily sentiment classification.

 Key Visualizations
Performance Distribution by Sentiment

Compares trader profitability across Fear vs Greed days.

Saved as:

outputs/chart_01_performance_boxplots.png
Trader Behavior Comparison

Measures behavioral changes across sentiment regimes:

trade frequency
leverage usage
position bias
average trade size

Saved as:

outputs/chart_02_behavior_comparison.png
Sentiment Impact by Trader Segments

Traders are segmented by:

leverage usage
trading frequency
win-rate consistency

PnL differences across sentiment regimes are analyzed for each segment.

Saved as:

outputs/chart_03_pnl_lev_sentiment.png
 Key Findings
 PnL shifts with sentiment

Average trader profitability differs between Fear and Greed market regimes.

Fear days mean PnL: ~$209k
Greed days mean PnL: ~$113k

However statistical testing suggests the difference is not statistically significant.

 Trader behavior changes during Fear

On Fear days traders tend to:

trade more frequently
slightly increase long exposure
use larger trade sizes

This suggests traders attempt to capture volatility rather than reduce risk.

 High-frequency traders dominate profitability

Most high-performing accounts fall into the frequent trading segment, indicating:

algorithmic or systematic trading behavior
active market making strategies
 Summary Statistics
Sentiment	Avg Trades	Avg Trade Size	Long Ratio
Extreme Greed	1083	5401	0.31
Fear	2017	6214	0.37
Greed	681	5953	0.33
Neutral	352	6528	0.40
 Strategy Implications
Risk Management during Fear Markets

High trading frequency during Fear periods suggests traders may overtrade volatility.

Risk controls such as:

leverage caps
smaller position sizing
volatility filters

may improve risk-adjusted returns.

Sentiment-aware trading strategies

Market sentiment can serve as a contextual signal for:

adjusting position sizing
controlling leverage exposure
modifying trade frequency
 Tech Stack
Python
Pandas
NumPy
Matplotlib
Seaborn
Jupyter Notebook
 Future Improvements

Possible extensions for deeper analysis:

time-series modeling of trader PnL
volatility-adjusted performance metrics
clustering trader strategies
machine learning prediction of profitable trading regimes
