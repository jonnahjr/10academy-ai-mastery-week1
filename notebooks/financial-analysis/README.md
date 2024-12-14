

# 📊 Financial Analysis Notebook

This Jupyter Notebook provides a comprehensive **financial analysis** using the `FinancialAnalyzer` class. The notebook covers key financial metrics, technical indicators, and portfolio optimization techniques.

---

## 📋 Table of Contents

1. [📈 Data Loading and Understanding](#-data-loading-and-understanding)  
2. [💡 Technical Indicator Calculations](#-technical-indicator-calculations)  
3. [📊 Data Visualization](#-data-visualization)  
4. [💼 Portfolio Optimization](#-portfolio-optimization)  
5. [🚀 How to Run the Notebook](#-how-to-run-the-notebook)  
6. [📜 License](#-license)  

---

## 📈 Data Loading and Understanding

### 1.1 Loading Stock Data
**Objective**: Load historical stock data for analysis.

**Steps**:
- Use the `load_stock_data(ticker)` method from the `FinancialAnalyzer` class to load historical stock data from a CSV file.

```python
# Example method to load stock data
data = FinancialAnalyzer.load_stock_data('AAPL')
```

### 1.2 Data Inspection
**Objective**: Understand the structure of the loaded data.

**Steps**:
- Inspect the first few rows and summarize the dataset to identify key features such as 'Open', 'Close', 'Volume', etc.

```python
# Inspect the first few rows
print(data.head())

# Summarize the dataset
print(data.describe())
```

---

## 💡 Technical Indicator Calculations

### 2.1 Simple Moving Average (SMA)
**Objective**: Calculate the **Simple Moving Average (SMA)** to smooth out price data.

**Steps**:
- Use the `calculate_moving_average(data, window_size)` method to calculate the SMA.

```python
# Calculate SMA with a 50-day window
sma = FinancialAnalyzer.calculate_moving_average(data, window_size=50)
```

### 2.2 Additional Technical Indicators
**Objective**: Calculate various technical indicators to analyze stock performance.

**Steps**:
- Use the `calculate_technical_indicators(data)` method to calculate indicators such as **SMA**, **RSI**, **EMA**, and **MACD**.

```python
# Calculate multiple technical indicators
indicators = FinancialAnalyzer.calculate_technical_indicators(data)
```

---

## 📊 Data Visualization

### 3.1 Plotting Stock Data with SMA
**Objective**: Visualize stock prices alongside the Simple Moving Average.

**Steps**:
- Use the `plot_stock_data(data)` method to create an interactive line plot.

```python
# Plot stock data with SMA
FinancialAnalyzer.plot_stock_data(data)
```

### 3.2 Plotting RSI, EMA, and MACD
**Objective**: Visualize additional technical indicators.

**Steps**:
- Use the `plot_rsi(data)`, `plot_ema(data)`, and `plot_macd(data)` methods to create interactive plots.

```python
# Plot RSI, EMA, and MACD
FinancialAnalyzer.plot_rsi(data)
FinancialAnalyzer.plot_ema(data)
FinancialAnalyzer.plot_macd(data)
```

---

## 💼 Portfolio Optimization

### 4.1 Calculating Optimal Portfolio Weights
**Objective**: Determine the optimal asset allocation for a portfolio.

**Steps**:
- Use the `calculate_portfolio_weights(tickers, start_date, end_date)` method to calculate the weights that maximize the Sharpe ratio.

```python
# Calculate optimal portfolio weights
weights = FinancialAnalyzer.calculate_portfolio_weights(['AAPL', 'GOOG', 'AMZN'], '2020-01-01', '2021-01-01')
print(weights)
```

### 4.2 Portfolio Performance Analysis
**Objective**: Evaluate the performance of the optimized portfolio.

**Steps**:
- Use the `calculate_portfolio_performance(tickers, start_date, end_date)` method to calculate the portfolio's return, volatility, and Sharpe ratio.

```python
# Calculate portfolio performance
performance = FinancialAnalyzer.calculate_portfolio_performance(['AAPL', 'GOOG', 'AMZN'], '2020-01-01', '2021-01-01')
print(performance)
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

---

## 📜 License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.  

---

### 🤝 Contributing

We welcome contributions! If you have ideas to improve this project:  

- Fork the repository  
- Create a new branch  
- Submit a pull request  

Thank you for your contributions! 🙌  

