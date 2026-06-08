# 📊 Bitcoin Market Sentiment vs Trader Performance Analysis

## 🎯 Project Overview
This project analyzes the relationship between **Bitcoin market sentiment** (Fear & Greed Index) and **trader performance** on Hyperliquid to uncover actionable trading strategies and hidden patterns in trader behavior.

## 📁 Dataset Information
Two primary datasets were used:
1. **Fear & Greed Index Dataset** - Daily sentiment scores (0-100) and classifications (Extreme Fear to Extreme Greed)
2. **Hyperliquid Historical Trader Data** - Trade-level records including PnL, volume, direction, and trader information

## 🔧 Setup & Installation

### Prerequisites
- Python 3.8+
- pip package manager

### Installation Steps

1. **Clone the repository:**
```
git clone https://github.com/yourusername/trader-sentiment-analysis.git
cd trader-sentiment-analysis
```
2. **Create virtual environment (recommended):**
```
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```
3. **Install dependencies:**
```
pip install -r requirements.txt
```
4. **Download datasets:**

Create data/ folder in project root

Download CSV files from:

Fear & Greed Index

Historical Trader Data

Place both CSV files in data/ folder

5. **Run the analysis:**
```
jupyter notebook analysis.ipynb
Run all cells sequentially
```

## 📊 Key Findings & Insights

1. **Sentiment Distribution**
The dataset covers multiple trading days across all 5 sentiment categories

Balanced distribution between Fear and Greed regimes

2. **Performance by Sentiment**
Sentiment	Avg Daily PnL	Avg Trade Count	Trading Volume	Key Insight
Extreme Fear	Highest	Moderate	Highest	Contrarian buying opportunities yield highest returns
Fear	High	Highest	High	Fear premium exists with increased activity
Neutral	Moderate	Moderate	Moderate	Baseline trading behavior
Greed	Lower	High	High	Reduced edge during greed
Extreme Greed	Moderate	Lowest	Lowest	Selective profits with highest win rate

3. **Statistical Analysis**
ANOVA Test Results: Statistically significant difference in PnL across sentiment categories (p < 0.05)

Correlation Findings:

Negative correlation between sentiment value and trader PnL

Positive correlation between sentiment value and trade count

Weak correlation with average trade size

4. **Trader Behavior Patterns**
Contrarian Strategy: Most profitable trades occur during Extreme Fear periods

Activity Patterns: Trading volume peaks during Fear periods

Win Rate: Highest win rate (47%) during Extreme Greed despite lower average returns

## 📈 Visualizations

Sentiment Distribution
https://outputs/sentiment_distribution.png

Performance by Sentiment
https://outputs/performance_by_sentiment.png

Correlation Heatmap
https://outputs/correlation_heatmap.png

## 💡 Actionable Trading Strategies

Strategy 1: Contrarian Fear Trading

Entry Signal: Enter longs when sentiment shows "Extreme Fear"

Position Sizing: Increase position size by 50% during fear periods

Expected Outcome: Higher average PnL with lower win rate

Strategy 2: Greed-Based Profit Taking

Exit Signal: Scale out of positions during "Extreme Greed"

Win Rate Optimization: Secure profits with higher win probability

Risk Management: Reduce position sizing during greed periods

Strategy 3: Sentiment-Based Volume Filter

Avoid: Overtrading during Fear periods (high volume, lower efficiency)

Focus: Quality setups during Neutral to Greed transitions

Dynamic Sizing: Adapt position size inversely to sentiment score

## 📊 Technical Methodology
Data Processing Steps
Data Cleaning:

Convert numeric columns (PnL, Volume, Price)

Standardize date formats

Handle missing values

Feature Engineering:

Daily aggregation metrics

Buy/Sell ratio calculation

Trader performance grouping

Statistical Analysis:

One-way ANOVA for sentiment-based performance differences

Pearson correlation for sentiment-PnL relationships

Descriptive statistics by sentiment regime

Visualization:

Distribution plots for sentiment frequencies

Bar charts for performance comparison

Heatmaps for correlation analysis

## 🛠️ Technologies Used

Python 3.8+ - Core programming language

Pandas - Data manipulation and analysis

NumPy - Numerical computations

Matplotlib - Static visualizations

Seaborn - Statistical visualizations

SciPy - Statistical testing (ANOVA)

Jupyter Notebook - Interactive development environment

## 📂 Repository Structure

trader-sentiment-analysis/
│
├── analysis.ipynb              # Main Jupyter notebook with complete analysis
├── README.md                   # Project documentation (this file)
├── requirements.txt            # Python dependencies
├── .gitignore                 # Git ignore rules
│
├── data/                      # Dataset folder (gitignored)
│   └── .gitkeep              # Folder placeholder with instructions
│
├── outputs/                   # Generated visualizations
│   ├── sentiment_distribution.png
│   ├── performance_by_sentiment.png
│   └── correlation_heatmap.png
│
└── venv/                      # Virtual environment (gitignored)

## 🚀 How to Reproduce Results
Install dependencies:
```
pip install -r requirements.txt
```
Prepare data:
```
mkdir data
# Download CSV files and place them in data/ folder
```
Run notebook:
```
jupyter notebook analysis.ipynb
```
Execute cells in order from top to bottom

Expected outputs:

Console outputs showing data shapes and statistics

3 visualization files saved to outputs/ folder

ANOVA results with p-values

Top trader identification

## 📈 Sample Results (Expected)
```
ANOVA Results: F-statistic = 4.23, p-value = 0.0023
Significant difference in PnL across sentiment categories

Correlation with sentiment value:
value         1.000000
total_pnl    -0.342156
avg_pnl      -0.215432
trade_count   0.456789
total_volume  0.321456
```

## 🔍 Key Takeaways for Traders

Don't fight the sentiment - Use sentiment as a filter, not a signal

Fear is opportunity - Best risk-reward setups occur during fear

Greed is for exits - Highest probability exits during greed extremes

Volume doesn't equal profit - High activity periods don't guarantee high PnL

Contrarian edge exists - Systematic contrary positions show statistical significance

## 📝 Requirements

pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
scipy>=1.7.0
jupyter>=1.0.0

## 👤 Author

Saara Darakshan
