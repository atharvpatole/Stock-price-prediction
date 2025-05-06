# 📈 Stock Price Prediction Using Machine Learning

This project aims to predict stock closing prices using machine learning models such as **Linear Regression**, **Decision Tree Regressor**, and **Random Forest Regressor**. It analyzes five years of historical stock data and compares model performance using **Mean Squared Error (MSE)**.

---

## 📂 Dataset

- **Name:** `all_stocks_5yr.csv`
- **Source:** [Kaggle - All Stocks 5 Year Data](https://www.kaggle.com/datasets)
- **Features:**
  - `date`
  - `open`, `high`, `low`, `close`
  - `volume`
  - `name` (stock symbol)
- **Duration:** 5 years of daily trading data for multiple publicly traded companies

---

## 🔧 Preprocessing

- Converted all column names to lowercase
- Parsed `date` column to datetime format
- Extracted `year` from the date
- One-hot encoded the `name` column (company names)
- Selected features: `open`, `high`, `low`, `volume`, `year`, and encoded company columns
- Split data: 80% training, 20% testing

---

## 🧠 Models Used

| Model              | Description                        |
|-------------------|------------------------------------|
| Linear Regression | Baseline model                     |
| Decision Tree     | Captures non-linear patterns       |
| Random Forest     | Ensemble of decision trees         |

---

## 📊 Evaluation Metric

- **Mean Squared Error (MSE)**
- Lower MSE indicates better prediction accuracy

### 🔍 Results:

| Model              | MSE      |
|-------------------|----------|
| Linear Regression | 20.89    |
| Decision Tree     | 4.13     |
| Random Forest     | 2.80     |

✅ **Random Forest** achieved the best performance.

---

## 🔎 Feature Importance

Top 10 most important features from the Random Forest model include:
- `low`, `high`, `open`, `volume`, `year`
- Encoded company names: `name_REGN`, `name_CMG`, `name_GOOG`, `name_GOOGL`, `name_AMZN`

---

## 📈 Visualizations

- Distribution of `open` and `close` prices
- Correlation heatmap
- Model comparison bar chart
- Feature importance bar chart
- Actual vs. Predicted line plot

---

## 🧪 Sample Output

![](images/model_comparison.png)  
_Model comparison based on MSE_

![](images/actual_vs_predicted.png)  
_Actual vs. predicted close prices using Random Forest_

---

## 📚 Future Work

- Use deep learning models like **LSTM** for sequential time-series prediction
- Incorporate external features such as market news, sentiment analysis, or macroeconomic indicators
- Hyperparameter tuning for improved accuracy

---

## 👥 Team Members

- Diya Farakte  
- Rishita Gupta  
- Srujal Shinde  
- Atharv Patole  

---

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).

