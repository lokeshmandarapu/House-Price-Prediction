# House-Price-Prediction

# 🏠 House Price Prediction – Ames Housing Data

This project involves predicting house prices using the Ames Housing dataset. We perform data cleaning, preprocessing, and apply regression models including Linear Regression, Ridge, and Lasso to identify the best fit. Evaluation is done using RMSE and R² metrics.

---

## 📊 Dataset Overview

- **Rows**: 2,930  
- **Features**: 251 (after encoding)  
- **Target**: `SalePrice` (final sale price of each home)

---

## 🧼 Data Cleaning Steps

- Dropped columns with more than 30% missing values  
- Filled missing numeric values with median  
- Filled missing categorical values with mode  
- One-hot encoded all categorical features (`drop_first=True`)  
- Final dataset: fully numeric and clean

---

## 🤖 Models & Results

| Model              | RMSE ($)     | R² Score |
|--------------------|--------------|----------|
| Linear Regression  | 29,152.88    | 0.89     |
| Ridge Regression   | 29,350.39    | 0.89     |
| Lasso Regression   | **28,904.22** ✅ | **0.90** ✅ |

✅ Lasso performed the best in terms of RMSE and R², despite a convergence warning (which can be resolved via feature scaling and increasing iterations).

---

## 📈 Visualizations

- Actual vs Predicted Price plots for all 3 models  
- Residual plot (Lasso) to visualize error patterns  
- Histogram of prediction errors

---

## 🧠 Tools Used

- **Python**, **Pandas**, **NumPy**  
- **Matplotlib**, **Seaborn**  
- **Scikit-learn** (`LinearRegression`, `Ridge`, `Lasso`, `train_test_split`, `metrics`)

---

## 🚀 How to Run

1. Clone the repo:
```bash
git clone https://github.com/lokeshmandarapu/house-price-prediction.git
