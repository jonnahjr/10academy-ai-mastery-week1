

# 🛠️ Utilities Used in the Project

This section provides an overview of the utilities used in the project, including functions for sentiment analysis and financial analysis tools that streamline stock data analysis and portfolio optimization.

---

## 📂 `utils.py`

### 1.1 Stock Sentiment Analysis
**Objective**: Perform sentiment analysis on stock-related data to assess the market sentiment for specific stocks.

**Function**: `stock_sentiment_analysis(sentiment_data: pd.DataFrame, stock_name: str)`  
- **Arguments**:
  - `sentiment_data`: A Pandas DataFrame object containing the sentiment analysis data.
  - `stock_name`: A string representing the stock that will be evaluated.

This function captures the data where the `stock_name` is found in the stock column and categorizes the sentiment score.

```python
# Example usage
stock_sentiment_analysis(sentiment_data, 'AAPL')
```

### 1.2 Sentiment Date Analysis
**Objective**: Similar to the stock sentiment analysis, but this function evaluates the range of dates covered by the sentiment data, providing the latest and earliest sentiment dates.

**Function**: `sentiment_date_analysis(sentiment_data: pd.DataFrame, stock_name: str)`  
- **Arguments**:
  - `sentiment_data`: A Pandas DataFrame object containing the sentiment data.
  - `stock_name`: A string representing the stock to analyze.

```python
# Example usage
sentiment_date_analysis(sentiment_data, 'AAPL')
```

---

## 📂 `financial_analyzer.py`

### Overview

This file contains the `FinancialAnalyzer` class designed to perform comprehensive financial analysis, integrating various financial data processing and analysis techniques. It allows users to load stock data, calculate technical indicators, visualize financial metrics, and perform portfolio optimization.

### Features

The `FinancialAnalyzer` class offers the following functionalities:

#### 1. **Load Stock Data**
   - Import historical stock data from CSV files.

#### 2. **Technical Indicators**
   - Calculate key technical indicators such as:
     - **Simple Moving Average (SMA)**
     - **Relative Strength Index (RSI)**
     - **Exponential Moving Average (EMA)**
     - **Moving Average Convergence Divergence (MACD)**

#### 3. **Data Visualization**
   - Plot stock prices and technical indicators using interactive charts.

#### 4. **Portfolio Optimization**
   - Calculate optimal portfolio weights and evaluate portfolio performance using the **Sharpe ratio**.

---

### Usage

To use the `FinancialAnalyzer` class:

1. **Import the class and necessary libraries**:
   ```python
   from financial_analyzer import FinancialAnalyzer
   import yfinance as yf
   ```

2. **Create an instance of the `FinancialAnalyzer` class**:
   ```python
   analyzer = FinancialAnalyzer()
   ```

3. **Load stock data**:
   ```python
   data = analyzer.load_stock_data('AAPL')
   ```

4. **Calculate technical indicators**:
   ```python
   sma = analyzer.calculate_moving_average(data, window_size=50)
   rsi = analyzer.calculate_rsi(data)
   ```

5. **Visualize the data**:
   ```python
   analyzer.plot_stock_data(data)
   analyzer.plot_rsi(data)
   ```

6. **Perform portfolio optimization**:
   ```python
   weights = analyzer.calculate_portfolio_weights(['AAPL', 'GOOG', 'AMZN'], '2020-01-01', '2021-01-01')
   performance = analyzer.calculate_portfolio_performance(['AAPL', 'GOOG', 'AMZN'], '2020-01-01', '2021-01-01')
   ```

---

### Requirements

To run the project, the following libraries are required:

- **Python 3.x**
- **Pandas**: For data manipulation and analysis.
- **yFinance**: To fetch historical stock data.
- **TA-Lib**: For calculating technical indicators.
- **Plotly**: For creating interactive visualizations.
- **PyPortfolioOpt**: For portfolio optimization.

To install the dependencies, use:

```bash
pip install -r requirements.txt
```

---

## 🚀 How to Run the Notebook

Follow these steps to run the analysis:

1. **Install Dependencies**  
   Ensure all required libraries are installed by running:
   ```bash
   pip install -r requirements.txt
   ```

2. **Open the Jupyter Notebook**  
   Open the notebook in your preferred environment (e.g., JupyterLab or VS Code).

3. **Run Each Cell Sequentially**  
   Execute each cell in the notebook to perform the analysis.
