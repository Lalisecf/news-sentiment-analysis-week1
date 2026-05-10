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
│   └── task_3_sentiment_correlation.ipynb
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

| Stock | Average Return | Volatility  | RSI Trend       |
| ----- | -------------- | ----------- | --------------- |
| AAPL  | Moderate       | Stable      | Neutral         |
| AMZN  | Moderate       | Medium      | Bullish         |
| GOOG  | Lower          | Most Stable | Bullish         |
| META  | Strong         | High        | Strong Momentum |
| NVDA  | Highest        | Highest     | Strong Momentum |

## Key Findings

* NVDA showed the highest returns and volatility
* META demonstrated strong bullish momentum
* GOOG was the most stable stock
* Market volatility increased significantly after 2020
* Technology-sector growth strongly influenced stock momentum

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
* task_3_sentiment_correlation.ipynb

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

---

# Future Work — Task 3

The next phase will focus on:

* sentiment analysis using NLP
* sentiment scoring of financial headlines
* date alignment between news and trading days
* Pearson correlation between sentiment and stock returns
* sentiment-return visualization and analysis

## Planned Tools

* NLTK VADER
* TextBlob

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

This project successfully established:

* a professional financial analytics workflow
* reusable stock analysis pipelines
* technical indicator computation for multiple stocks
* exploratory analysis of financial news data

The analysis identified strong momentum in AI-driven technology companies and laid the foundation for sentiment-driven predictive market analysis.

Future sentiment correlation analysis will extend the project by connecting financial news narratives directly to stock price movements.

---

# References

* yfinance Documentation
* TA-Lib Python Documentation
* TextBlob Documentation
* NLTK Documentation
* scikit-learn Documentation
