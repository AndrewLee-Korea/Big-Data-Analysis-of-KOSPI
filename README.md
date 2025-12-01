# 📈 Big-Data-Analysis-of-KOSPI

This project analyzes the **correlation between credit balance indicators in the capital market and the KOSPI index** using Python-based big data analytics.

> Analysis Period: From 2008  
> Targets: Daily KOSPI index, margin trading credit balance, secured loan balance  
> Technologies: Python, pandas, matplotlib, scikit-learn, TensorFlow

---

## 📌 Objective

- Empirically analyze the **impact of margin trading activities** (e.g., credit loan, short selling) on the **KOSPI index**
- Evaluate **correlation and predictability** using regression and machine learning models

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

## 🔍 Analysis Steps

1. **Exploratory Data Analysis & Preprocessing**
   - Check for null values, normalize data, create new features
   - Correlation matrix among variables

2. **Visualization**
   - KOSPI trend over time
   - Scatter plots and correlation matrix

3. **Regression Analysis**
   - Simple Linear Regression (e.g., credit_long → KOSPI)
   - Multiple Linear Regression (e.g., lending + credit_long → KOSPI)
   - Model Evaluation: R², RMSE

4. **Machine Learning**
   - Gradient Descent-based regression using TensorFlow
   - Achieved high predictive performance without hyperparameter tuning

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

## 📌 References

- [KRX Market Data](http://marketdata.krx.co.kr/)
- [KOFIA Statistical Data](https://freesis.kofia.or.kr)

---

## 🏷️ License

This project was created for academic and analytical purposes. No specific license is applied.
