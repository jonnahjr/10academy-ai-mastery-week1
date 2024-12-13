<<<<<<< HEAD
# Financial News Sentiment and Stock Price Analysis

## Overview

- This project explores the relationship between **financial news sentiment** and **stock price movements.** It leverages various data analysis techniques, including **exploratory data analysis (EDA)**, **sentiment analysis**, and **correlation analysis**, to investigate how news sentiment influences stock prices. The project is part of the **Week 1 Challenge of the 10 Academy AI Mastery program.**

## Project Structure

* **.vscode/** : Contains personal development environment configuration settings for vscode.
* **notebooks/** : Jupyter notebooks used for analysis and visualization.
* **.github/workflows/** : CI/CD pipeline configuration with GitHub Acti

## Key Tasks

1. **Exploratory Data Analysis (EDA)** : Analyze the dataset to extract key statistics and identify patterns including **Sentiment Analysis** and **Time Series Analysis**
2. **Stock Price Analysis** : Analyze stock price data using technical indicators.
3. **Correlation Analysis** : Investigate the correlation between news sentiment and stock price movements.

- *All details about the analysis are found in `notebooks/README.md`*

## Usage

1. Run the Jupyter notebooks in the `notebooks/` directory to perform analysis.

## Contributions

Feel free to open issues or submit pull requests to improve the project.

## License

This project is licensed under the **Creative Commons Legal Code**
=======


# 🌟 **10 Academy: Artificial Intelligence Mastery Challenge - Week 1** 🌟

**_Financial News Sentiment Analysis & Stock Price Movement Correlation_**

Welcome to the repository of my project for the **10 Academy: Artificial Intelligence Mastery Challenge - Week 1**. This project dives deep into analyzing the relationship between **financial news sentiment** and **stock price movements** of major tech companies, exploring how financial news shapes market behavior. The challenge is not only a technical venture but a journey into understanding the power of sentiment in the financial markets.

---

## 📖 **Challenge Overview**

In this week’s challenge, I focused on correlating **financial news sentiment** with **stock price movements** of prominent companies such as:

- **Apple (AAPL)**
- **Amazon (AMZN)**
- **Google (GOOG)**
- **Meta (META)**
- **Microsoft (MSFT)**
- **NVIDIA (NVDA)**
- **Tesla (TSLA)**

By performing **sentiment analysis** on real-time and historical financial news headlines, we uncover insights into how sentiment can predict stock price behavior. The analysis included various **technical indicators** to measure trends and identify any patterns between news sentiment and market movements.

---

## 🛠️ **Tech Stack**

This project uses a modern tech stack to combine **data science**, **sentiment analysis**, and **financial prediction**. Here’s the breakdown:

- **Python**: The primary programming language for data manipulation, analysis, and machine learning.
- **pandas**: For powerful data manipulation and analysis.
- **TA-Lib**: Technical analysis library to calculate stock market indicators like moving averages and RSI.
- **TextBlob**: Sentiment analysis on financial news headlines.
- **nltk**: Natural Language Toolkit for deeper text processing.
- **Matplotlib** & **Seaborn**: Beautiful data visualizations that highlight key patterns.
- **pynance**: A specialized library to access financial data and perform stock analysis.

---

## 🚀 **Project Workflow**

### **1. Data Collection**
We collected stock price data for major companies and linked relevant financial news headlines to these prices to provide meaningful context.

### **2. Data Processing**
- Cleaned and merged the stock price data with the news data.
- Preprocessed and normalized both the text data (news headlines) and the stock price data.

### **3. Sentiment Analysis**
We used **TextBlob** and **nltk** to extract sentiment scores from the news headlines. These scores were later used to analyze the impact of sentiment on stock price movements.

### **4. Correlation Analysis**
We applied **TA-Lib** to compute technical indicators (e.g., RSI, moving averages) and visualized the correlations between sentiment and stock price movements.

### **5. Data Visualization**
We used **Matplotlib** and **Seaborn** to create stunning visualizations that reveal insights about how news sentiment correlates with stock price movements.

---

## 💡 **Key Findings & Insights**

- **Positive Sentiment Impact**: Positive sentiment in news correlates strongly with upward stock price movements.
- **Negative Sentiment Influence**: Negative sentiment tends to drive stock prices down, especially during periods of earnings announcements.
- **Publisher Impact**: Major news outlets such as **Reuters** and **Bloomberg** show a significant impact on stock movements.
- **Market Time Sensitivity**: Sentiment closer to market opening times has a more profound effect on stock prices.

---

## 📊 **Visualizations**

The following visualizations provide insights into how sentiment correlates with stock market behavior:

- **Stock Price vs Sentiment**:
    - A line plot shows the change in stock price over time with sentiment scores overlaid.

- **RSI and Moving Averages**:
    - The RSI and 50-day moving average indicators are plotted to predict stock price trends.

- **Sentiment & Stock Movement Correlation**:
    - A heatmap showing the strength of correlation between sentiment and stock price movements.

- **Scatter Plots**:
    - Scatter plots highlight the relationship between sentiment scores and daily stock returns.

---

## ⚙️ **Getting Started**

To run this project locally on your machine, follow these simple steps:

### 1. **Clone the Repository**

```bash
git clone https://github.com/jonnahjr/10academy-ai-mastery-week1.git
cd 10academy-ai-mastery-week1
```

### 2. **Install Dependencies**

Install the required Python packages using `pip`:

```bash
pip install -r requirements.txt
```

### 3. **Run Jupyter Notebooks**

Explore the **Jupyter notebooks** for a step-by-step analysis of the data:

```bash
jupyter notebook
```

### 4. **Run Scripts**

Execute the analysis by running the Python scripts in the `scripts/` folder:

```bash
python sentiment_analysis.py
python correlation_analysis.py
```

---

## 💻 **Contributing**

This project is open to contributions! If you have any ideas or improvements, feel free to fork the repository and submit a pull request. Please ensure that your code is well-documented and passes the tests.

---

## 📂 **Directory Structure**

Here’s the organized structure of the repository:

```
├── .vscode/                   # VSCode configuration
├── .github/                   # GitHub workflows
├── requirements.txt           # Python dependencies
├── README.md                  # Project documentation
├── src/                       # Core source code
│   └── __init__.py
├── notebooks/                 # Jupyter notebooks for data analysis
├── scripts/                   # Python scripts for analysis
├── tests/                     # Unit tests and testing scripts
└── data/                      # Collected data (financial news & stock prices)
```

---

## 🎯 **Acknowledgments**

A huge thank you to:

- **10 Academy** for creating this amazing learning platform.
- **TA-Lib** and **pynance** for their incredible libraries for financial analysis.
- **TextBlob** and **nltk** for making sentiment analysis so straightforward.
- **Matplotlib** and **Seaborn** for their beautiful visualizations.

---


---

### ✨ **Thank you for visiting!** ✨
>>>>>>> 0143906f65d5c4fe3606420ed5fc4f1728ea7a64
