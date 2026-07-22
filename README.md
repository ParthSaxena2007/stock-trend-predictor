# 📈 Stock Trend Predictor

A machine learning project that predicts the **next day's stock price direction (Up/Down)** using historical market data and technical indicators. This project implements a complete end-to-end ML pipeline—from data collection and feature engineering to model training, evaluation, visualization, and prediction.

The objective is to compare multiple machine learning algorithms and analyze how well they classify the future movement of stock prices using technical analysis features.

---

## 🚀 Features

- Historical stock data collection using **Yahoo Finance**
- Automatic data preprocessing and cleaning
- Engineering of **25 technical indicators** and market features
- Binary classification for **next-day price movement**
- Comparison of multiple machine learning models
- Comprehensive model evaluation using multiple metrics
- Visualizations for exploratory data analysis and model performance
- Trained models saved for future inference

---

## 🧠 Machine Learning Pipeline

```
Historical Stock Data
        │
        ▼
Data Cleaning & Preprocessing
        │
        ▼
Feature Engineering
        │
        ▼
Train-Test Split
        │
        ▼
Feature Scaling
        │
        ▼
Model Training
        │
        ▼
Model Evaluation
        │
        ▼
Prediction
```

---

# 📂 Project Structure

```
stock-trend-predictor/
│
├── data/
│   ├── titan_10y_cleaned.csv
│   ├── final_df_for_ml.csv
│   ├── X.csv
│   └── y.csv
│
├── models/
│   ├── logistic_regression.pkl
│   ├── random_forest.pkl
│   ├── xgboost.pkl
│   └── scaler.pkl
│
├── notebooks/
│   └── Stock_Trend_Predictor.ipynb
│
├── plots/
│   ├── correlation_heatmap.png
│   ├── confusion_matrix.png
│   ├── roc_curve.png
│   ├── feature_importance.png
│   └── ...
│
├── src/
│   └── stock_trend_predictor/
│       └── __init__.py
│
├── README.md
├── requirements.txt
├── .gitignore
└── main.py
```

---

# 📊 Dataset

The project uses approximately **10 years of daily stock market data** downloaded using the **Yahoo Finance API (`yfinance`)**.

Example columns include:

- Open
- High
- Low
- Close
- Adjusted Close
- Volume

After preprocessing and feature engineering, the dataset is transformed into a machine learning-ready format.

---

# ⚙️ Feature Engineering

The model is trained using **25 engineered features**, including:

### Price-Based Features

- Daily Return
- Open-Close Change
- Rate of Change (ROC)
- Return Lag Features

### Trend Indicators

- SMA Distance (20, 50, 200)
- MACD Histogram
- RSI (14)

### Volatility Indicators

- ATR Percentage
- Bollinger Band Width
- True Range

### Volume Indicators

- Volume Moving Average
- Volume Change Ratio
- On Balance Volume (OBV)
- OBV Slope
- Chaikin Money Flow (CMF)

### Liquidity Features

- Kyle's Lambda Proxy
- Rolling Kyle's Lambda

---

# 🎯 Prediction Target

The task is formulated as a **binary classification problem**.

| Target | Meaning |
|---------|---------|
| 1 | Next day's closing price is higher than today's |
| 0 | Next day's closing price is lower or equal to today's |

---

# 🤖 Machine Learning Models

The following models are implemented and compared:

- Logistic Regression
- Random Forest Classifier
- XGBoost Classifier

Each model is trained on the same feature set to provide a fair performance comparison.

---

# 📈 Evaluation Metrics

Model performance is evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC Score
- Confusion Matrix
- ROC Curve

These metrics provide a comprehensive assessment of classification performance.

---

# 📉 Visualizations

The project includes multiple visualizations to understand both the dataset and model performance.

Examples include:

- Stock Price Trend
- Correlation Heatmap
- Confusion Matrix
- ROC Curve
- Feature Importance
- Model Comparison Charts

---

# 🛠️ Technologies Used

### Programming Language

- Python

### Libraries

- pandas
- numpy
- matplotlib
- scikit-learn
- xgboost
- yfinance
- ta
- joblib

---

# ▶️ Installation

Clone the repository:

```bash
git clone https://github.com/your-username/stock-trend-predictor.git
```

Move into the project directory:

```bash
cd stock-trend-predictor
```

Install the required packages:

```bash
pip install -r requirements.txt
```

---

# ▶️ Usage

Run the Jupyter notebook:

```bash
jupyter notebook
```

Open:

```
notebooks/Stock_Trend_Predictor.ipynb
```

Run all cells sequentially to:

- Download and preprocess stock data
- Generate technical indicators
- Train machine learning models
- Evaluate model performance
- Save trained models

---

# 💾 Saved Models

The trained models are stored inside the `models/` directory.

- Logistic Regression
- Random Forest
- XGBoost
- Standard Scaler

These can be loaded directly for future predictions without retraining.

---

# 🔮 Future Improvements

Potential extensions of this project include:

- Support for multiple stocks simultaneously
- Hyperparameter optimization
- LSTM and Transformer-based deep learning models
- Real-time prediction using live market data
- Streamlit or Flask web application
- Portfolio optimization using predicted signals
- Automated backtesting strategy
- Explainable AI using SHAP values

---

# 📚 Learning Outcomes

This project demonstrates practical experience in:

- Data preprocessing
- Feature engineering
- Technical analysis
- Machine learning pipelines
- Classification algorithms
- Model evaluation
- Data visualization
- Model serialization
- Reproducible project organization

---

# 📄 License

This project is intended for educational and research purposes.

---

## ⭐ Acknowledgements

- Yahoo Finance (`yfinance`) for historical market data
- Scikit-learn for machine learning utilities
- XGBoost for gradient boosting implementation
- Open-source Python ecosystem for data analysis and visualization
