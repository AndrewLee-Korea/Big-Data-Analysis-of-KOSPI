# 📈 Big-Data-Analysis-of-KOSPI

This project investigates the relationship between margin trading activity and stock market performance in the Korean capital market. Using daily data from 2008 to 2018, I apply regression analysis and machine learning techniques to quantify how credit balance indicators correlate with and potentially predict KOSPI index movements.

---

## 📌 Motivation

Margin trading—where investors borrow funds or securities to amplify their positions—serves as a barometer of market sentiment. In Korea's capital market, debates around short selling regulations and institutional lending practices have intensified, yet empirical analysis of how margin activities relate to index performance remains limited.
This project addresses a key research question: To what extent do credit balance indicators (margin loans, securities lending, secured loans) correlate with KOSPI index movements, and can these indicators serve as predictive features?

---

## Key Findings

| Model | R² (Test) | RMSE |
|-------|-----------|------|
| Simple Linear Regression (credit_long) | 0.45 | 212.5 |
| Simple Linear Regression (lending) | 0.68 | 162.8 |
| **Multiple Linear Regression (lending + credit_long)** | **0.80** | **126.8** |
| TensorFlow Gradient Descent | ~0.80 | ~127 |

---

## 🧩 Data Overview

| Variable Name     | Description                          |
|-------------------|--------------------------------------|
| `Time`            | Date                                 |
| `kospi_price`     | KOSPI index                          |
| `lending`         | Margin loan balance                  |
| `credit_long`     | Long position credit balance         |
| `credit_short`    | Short position credit balance        |
| `secured_loan`    | Secured loan balance                 |
| `*_gr`            | Growth rates of each variable        |

Source CSV: `project_data2.csv`

---

## 🔍 Methodology

1. **Exploratory Data Analysis & Preprocessing**
   - Merged multiple data sources on trading dates
   - Verified data integrity (no missing values across 2,460 observations)
   - Computed daily growth rates for all variables
   - Generated correlation matrix and scatter plot visualizations

2. **Regression Analysis**
   - Simple Linear Regression: Individual predictors (credit_long, lending) against KOSPI
   - Multiple Linear Regression: Combined predictors for improved R²
   - Train/Test Split: 70/30 ratio with fixed random seed for reproducibility
   - Evaluation Metrics: R² (coefficient of determination), RMSE

3. **Machine Learning**
   - Implemented gradient descent optimization using TensorFlow 1.x
   - Achieved comparable performance to scikit-learn models
   - Demonstrated scalability for larger datasets

---

## 📊 Key Findings

- `credit_long` and `lending` have strong positive correlation with the KOSPI index (R² > 0.8)
- With multiple regression, test R² ≈ **0.80**, RMSE ≈ **126.8**
- Size of margin trading activities indicates strong investor sentiment, reflected in index movements

---

## 🛠 Libraries Used

```python
pandas
matplotlib
numpy
scikit-learn
tensorflow (v1.x)
```

---

## 🛠 Requirements
pandas>=0.23.0
numpy>=1.14.0
matplotlib>=2.2.0
scikit-learn>=0.19.0
tensorflow>=1.8.0,<2.0.0

---

## 📁 Project Structure

```
.
├── Anal_Cor_Credit_balance_Index.ipynb  # Jupyter Notebook
├── project_data2.csv                    # Input data
├── README.md                            # Project documentation
```

---

## 🧠 Contributor

- **Yongjun Lee** (Korea Securities Finance Corporation)  
  - Data collection & preprocessing  
  - Regression modeling and interpretation  
  - Machine learning model design and evaluation  

---

## 📌 Data sources

- [KRX Market Data](http://marketdata.krx.co.kr/)
- [KOFIA Statistical Data](https://freesis.kofia.or.kr)

---

## 🏷️ License

This project was created for academic and analytical purposes. No specific license is applied.
