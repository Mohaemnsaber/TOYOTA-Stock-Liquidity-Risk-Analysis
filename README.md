# 🚗 TOYOTA Stock Liquidity Risk Analysis

This project focuses on detecting **liquidity risk** in TOYOTA stock using a machine learning classification approach. It identifies **illiquid trading days** based on historical volume and price data.

---

## 📊 Dataset

- **Source:** [TOYOTA.csv]
- **Rows:** 11,415
- **Columns:** `date`, `open`, `high`, `low`, `close`, `adj_close`, `volume`
- **Target Variable:** `illiquid_day` (1 = low liquidity, 0 = normal liquidity)

---

## 🔁 Workflow

### 1. Data Cleaning
- Converted `volume` and `close` columns to numeric
- Replaced 0s and invalid strings with `NaN`
- Dropped missing rows

### 2. Feature Engineering
- `log_volume`: Log-transformed volume
- `volume_ma_5`: 5-day moving average
- `volume_std_5`: 5-day volatility (std deviation)
- `illiquid_day`: Binary label for low liquidity (below 25th percentile)

### 3. Modeling
- **Logistic Regression**
- **Random Forest**
- **XGBoost**

### 4. Evaluation Metrics
- Confusion Matrix
- Accuracy
- Precision, Recall, F1-Score
- ROC AUC Score

---

## 🏆 Model Performance

| Model               | Accuracy | ROC AUC |
|---------------------|----------|---------|
| Logistic Regression | 99.91%   | 0.9988  |
| Random Forest       | 100%     | 1.0000  |
| XGBoost             | 99.87%   | 0.9980  |

✅ **Stratified cross-validation accuracy (Logistic Regression):** 99.75%

---

## 📈 Feature Importance

Both **Random Forest** and **XGBoost** identified `log_volume` and `volume volatility` as key indicators of illiquid days.

---

## 🔧 Tech Stack

- Python
- pandas, numpy, matplotlib, seaborn
- scikit-learn
- XGBoost

---

## 🧠 Author

Mohaemn Saber  
📧 mohaemn.saber@gmail.com.com 
🔗 [LinkedIn](www.linkedin.com/in/mohaemn-saber-41364b255) 

---

## 📂 Project Structure

TOYOTA-Liquidity-Risk/
│
├── TOYOTA.csv
├── liquidity_risk_model.ipynb
├── README.md
└── requirements.txt


---

## 📌 License

This project is open-source and available under the [MIT License](LICENSE).

