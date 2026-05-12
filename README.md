# Predicting Price Moves with News Sentiment

![CI](https://github.com/your-username/news-sentiment-analysis/actions/workflows/unittests.yml/badge.svg)

Financial markets react rapidly to news headlines, earnings announcements, analyst upgrades, and macroeconomic events. This project analyzes the relationship between financial news sentiment and stock market behavior using Natural Language Processing (NLP) and quantitative financial analysis.

This project was completed as part of the **10 Academy Artificial Intelligence Mastery – Week 1 Challenge**.

---

# Business Objective

The goal of this project is to help **Nova Financial Solutions** improve predictive analytics capabilities by:

* analyzing financial news sentiment
* computing technical indicators from historical stock data
* identifying relationships between sentiment and stock price movements
* generating data-driven investment insights

---

# Stocks Analyzed

* AAPL
* AMZN
* GOOG
* META
* NVDA

---

# Repository

GitHub Repository: [Add Your GitHub Repository Link Here]

---

# Project Structure

```bash
news-sentiment-analysis/
│
├── .github/
│   └── workflows/
│       └── unittests.yml
│
├── data/
│   └── raw/
│
├── notebooks/
│   ├── task_1_eda.ipynb
│   ├── task_2_quantitative_analysis.ipynb
│   └── task_3_sentiment_stock_correlation.ipynb
│
├── scripts/
├── src/
├── tests/
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

# Task 1 — Exploratory Data Analysis (EDA)

## Objectives

* Set up GitHub workflow and CI/CD
* Explore the financial news dataset
* Analyze publishers and publication trends
* Perform keyword and topic analysis

## Analyses Performed

* Headline length distribution
* Publisher activity analysis
* News publication trends over time
* Publishing time analysis
* TF-IDF keyword extraction
* WordCloud visualization
* Publisher domain analysis

## Key Insights

* Financial headlines are concise and highly structured
* News volume spikes around earnings announcements and major events
* Technology and AI-related narratives dominate financial news
* A small number of publishers contribute most articles
* Most financial news is released during active trading hours

---

# Task 2 — Quantitative Financial Analysis

## Objectives

* Load and clean historical stock data
* Compute technical indicators
* Build reusable stock analysis pipelines
* Compare stock performance metrics

## Technical Indicators Computed

* Simple Moving Average (SMA)
* Exponential Moving Average (EMA)
* Relative Strength Index (RSI)
* Moving Average Convergence Divergence (MACD)

## Quantitative Summary

| Stock | Average Return | Volatility | RSI Trend |
| ----- | -------------- | ---------- | --------- |
| AAPL  | Moderate       | Stable     | Neutral |
| AMZN  | Moderate       | Medium     | Bullish |
| GOOG  | Lower          | Most Stable | Bullish |
| META  | Strong         | High       | Strong Momentum |
| NVDA  | Highest        | Highest    | Strong Momentum |

## Key Findings

* NVDA showed the highest returns and volatility
* META demonstrated strong bullish momentum
* GOOG was the most stable stock
* Market volatility increased significantly after 2020
* Technology-sector growth strongly influenced stock momentum

---

# Task 3 — Correlation Between News Sentiment and Stock Movement

## Objectives

* Perform sentiment analysis on financial news headlines
* Generate numerical sentiment scores using NLP
* Align financial news dates with stock trading days
* Compute daily stock returns
* Measure correlation between sentiment and stock price movement
* Visualize sentiment-return relationships
* Interpret correlation strength and limitations

## Sentiment Analysis Tool

This project used **NLTK VADER (Valence Aware Dictionary and Sentiment Reasoner)** for sentiment analysis.

### Why VADER?

VADER was selected because:
* it performs well on short text such as news headlines,
* it is lightweight and computationally efficient,
* and it produces normalized sentiment scores between -1 and +1.

The compound sentiment score was used as the primary sentiment metric.

## Task 3 Workflow

### Date Alignment

* Converted publication timestamps into datetime format
* Matched news headlines with stock trading dates
* Handled missing and unmatched records
* Aligned non-trading day articles to available trading dates

### Sentiment Scoring

Each headline received a sentiment score:
* Positive sentiment → closer to +1
* Negative sentiment → closer to -1
* Neutral sentiment → near 0

### Daily Sentiment Aggregation

When multiple headlines existed for the same stock on the same day:
* average daily sentiment scores were calculated

### Daily Return Calculation

Daily stock returns were computed using:

\[
\text{Daily Return}_t =
\frac{\text{Close}_t - \text{Close}_{t-1}}
{\text{Close}_{t-1}}
\times 100
\]

### Correlation Analysis

Pearson correlation analysis was used to measure the relationship between:
* average daily sentiment scores
* and daily stock returns

---

# Correlation Results

| Stock | Correlation | Interpretation |
|---|---|---|
| NVDA | 0.207 | Strongest positive relationship |
| GOOG | 0.171 | Moderate positive relationship |
| AMZN | 0.161 | Weak positive relationship |
| AAPL | 0.120 | Weakest positive relationship |

## Key Findings

* All analyzed stocks showed positive sentiment-return correlations
* NVDA demonstrated the strongest sentiment sensitivity
* GOOG also showed statistically meaningful sentiment relationships
* AAPL and AMZN exhibited weaker relationships
* META had insufficient aligned observations for reliable analysis

Overall, the findings suggest that positive financial news sentiment generally aligns with positive stock returns, although the relationship remains relatively weak.

---

# Interpretation of Results

## Correlation Interpretation

The analysis explored the relationship between financial news sentiment and daily stock price movement using Pearson correlation coefficients.

The results showed weak positive correlations across the analyzed technology stocks.

Positive correlation values indicate that positive financial news sentiment generally aligned with positive daily stock returns.

Among the analyzed stocks:
* NVDA showed the strongest relationship between sentiment and stock movement
* GOOG also demonstrated a noticeable positive relationship
* AAPL and AMZN exhibited weaker positive correlations

The scatter plots further confirmed that although positive sentiment sometimes aligned with positive returns, the data points remained widely dispersed, indicating that sentiment alone is not a strong predictor of stock price movement.

The p-values also suggested that:
* NVDA and GOOG produced statistically significant relationships
* AAPL and AMZN showed weaker statistical significance

Overall, the findings suggest that financial news sentiment may provide useful predictive signals when combined with technical indicators and broader market analysis techniques.

---

# Limitations

Several limitations should be considered when interpreting the results of this analysis:

* Correlation does not imply causation
* Market prices are influenced by many external factors
* News impact may occur with lag effects
* Headlines alone may not capture full article sentiment
* Financial sentiment models may misinterpret technical language
* Some stocks had insufficient aligned observations after merging datasets

---

# Investment Strategy Recommendations

Based on the findings:

* Use sentiment analysis as a supplementary trading signal
* Combine sentiment with technical indicators such as RSI and MACD
* Focus on stocks with stronger sentiment-return relationships
* Explore lag-based sentiment analysis for future improvements
* Use rolling correlations to monitor changing market behavior

---

# Technologies Used

## Programming & Analysis

* Python 3.11
* pandas
* numpy
* matplotlib
* seaborn

## NLP & Machine Learning

* scikit-learn
* nltk
* NLTK VADER
* TextBlob
* wordcloud

## Financial Analysis

* yfinance
* ta
* pynance

## Development Tools

* Git
* GitHub
* GitHub Actions
* Jupyter Notebook

---

# Installation

## Clone Repository

```bash
git clone <your-repository-url>
cd news-sentiment-analysis
```

## Create Virtual Environment

```bash
python -m venv venv
```

## Activate Environment

### Windows

```bash
venv\Scripts\activate
```

### Linux / Mac

```bash
source venv/bin/activate
```

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# Running the Project

## Launch Jupyter Notebook

```bash
jupyter notebook
```

## Open the notebooks

* task_1_eda.ipynb
* task_2_quantitative_analysis.ipynb
* task_3_sentiment_stock_correlation.ipynb

---

# Running Tests

To run tests locally:

```bash
pytest
```

GitHub Actions automatically runs CI checks on push and pull requests.

---

# Reusable Stock Analysis Pipeline

The project includes a reusable workflow that:

* automatically loads stock CSV files
* computes technical indicators
* performs sentiment analysis
* generates visualizations
* summarizes financial metrics

## Supported Stocks

* AAPL
* AMZN
* GOOG
* META
* NVDA

---

# Sample Visualizations

The project generates:

* stock price charts with SMA & EMA overlays
* RSI momentum charts
* MACD crossover charts
* publication frequency trends
* publisher activity plots
* WordCloud keyword visualizations
* sentiment vs return scatter plots
* sentiment category return bar charts

---

# Contribution Guidelines

Contributions and improvements are welcome.

## Workflow

1. Create a new feature branch
2. Commit changes using descriptive commit messages
3. Open a pull request before merging into main

### Example

```bash
git checkout -b feature-name
git commit -m "feat: add RSI analysis"
```

---

# Conclusion

This project successfully integrated financial news analysis with quantitative stock market analysis.

The project achieved:
* exploratory analysis of financial news data
* technical indicator computation
* sentiment scoring of financial headlines
* stock return analysis
* statistical correlation analysis between sentiment and market movement

The findings suggest that financial news sentiment can provide valuable predictive insights when combined with technical and quantitative market analysis techniques.

This project demonstrates how Natural Language Processing (NLP) and financial analytics can be integrated to support data-driven investment decision-making.

---

# References

* yfinance Documentation
* TA-Lib Python Documentation
* TextBlob Documentation
* NLTK Documentation
* scikit-learn Documentation
* VADER Sentiment Documentation