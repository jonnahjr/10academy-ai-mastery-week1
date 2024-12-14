
# 📰 Exploratory Data Analysis (EDA) on News Dataset

This repository contains an in-depth **Exploratory Data Analysis (EDA)** of a news dataset. The project covers various analyses such as descriptive statistics, sentiment analysis, time series analysis, and publisher contributions. The goal is to uncover insights about headline characteristics, publication trends, and sentiments.

---

## 📋 Table of Contents

1. [📊 Data Understanding](#-data-understanding)  
2. [📈 Descriptive Statistics](#-descriptive-statistics)  
3. [💬 Text Analysis / Sentiment Analysis](#-text-analysis--sentiment-analysis)  
4. [📅 Time Series Analysis (TSA)](#-time-series-analysis-tsa)  
5. [📰 Publisher Analysis](#-publisher-analysis)  
6. [🚀 How to Run the Notebook](#-how-to-run-the-notebook)  
7. [📜 License](#-license)  

---

## 📊 Data Understanding

Before starting the analysis, we need to understand the **structure and content** of the dataset. This involves loading the data and inspecting the first few rows to identify key features.

### 🛠️ Load Data

```python
import pandas as pd

# Path to the CSV file
file_path = 'Path_to_the_csv_file'

# Load the dataset
df = pd.read_csv(file_path)

# Display the first few rows
print(df.head())
```

---

## 📈 Descriptive Statistics

Descriptive statistics summarize the **central tendency**, **dispersion**, and **distribution** of the dataset. Key steps include:

- 📏 **Headline Length Distribution**
- 📰 **Article Count per Publisher**
- 📆 **Publication Date Analysis**

### 📝 Headline Length Distribution

```python
# Calculate headline lengths
df['headline_length'] = df['headline'].apply(len)

# Display basic statistics for headline lengths
headline_stats = df['headline_length'].describe()
print(headline_stats)
```

### 📰 Count Articles per Publisher

```python
# Count articles by publisher
publisher_counts = df['publisher'].value_counts()
print(publisher_counts)
```

### 📆 Publication Dates

```python
# Convert the 'date' column to datetime
df['date'] = pd.to_datetime(df['date'])

# Display publication date statistics
print(df['date'].describe())
```

---

## 💬 Text Analysis / Sentiment Analysis

Sentiment analysis helps uncover whether the sentiment behind a headline is **positive**, **negative**, or **neutral**. This section calculates a polarity score for each headline.

### ✍️ Perform Sentiment Analysis

```python
from textblob import TextBlob

# Apply sentiment analysis
df['sentiment'] = df['headline'].apply(lambda x: TextBlob(x).sentiment.polarity)

# Display sentiment statistics
print(df['sentiment'].describe())
```

---

## 📅 Time Series Analysis (TSA)

**Time Series Analysis** examines publication trends over time. Insights into the frequency of articles during specific periods or events can be derived.

### 📆 Resample Data by Day & Plot

```python
import matplotlib.pyplot as plt

# Set date as the index
df.set_index('date', inplace=True)

# Resample data by day and count articles
daily_articles = df['headline'].resample('D').count()

# Plot the number of articles over time
plt.figure(figsize=(10, 5))
daily_articles.plot()
plt.title("📅 Number of Articles Published Over Time")
plt.xlabel("Date")
plt.ylabel("Number of Articles")
plt.show()
```

🛠️ **Detailed TSA**: Refer to `./TSA/TAS_headline.ipynb` for advanced analysis.

---

## 📰 Publisher Analysis

This section explores the contributions of different publishers to identify the most active contributors and their impact on the dataset.

### 📊 Contribution Analysis

```python
# Calculate the percentage contribution of each publisher
publisher_contribution = df['publisher'].value_counts(normalize=True) * 100

# Display top contributors
print(publisher_contribution.head())
```

---

## 🚀 How to Run the Notebook

Follow these steps to run the analysis:

1. **Install Dependencies**  
   Ensure all required libraries are installed:
   ```bash
   pip install -r requirements.txt
   ```

2. **Open the Jupyter Notebook**  
   Open the notebook in your preferred environment (e.g., JupyterLab or VS Code).

3. **Run Each Cell Sequentially**  
   Execute each cell in the notebook to perform the analysis.
