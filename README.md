# 🏠 House Price Prediction - Seattle Dataset

This project focuses on predicting house prices using **Linear Regression**, **Ridge Regression**, and **Lasso Regression** on a real-world housing dataset from Seattle.

---

## 📁 Dataset Source

The dataset used in this project comes from Kaggle:

**[Seattle House Price Dataset on Kaggle](https://www.kaggle.com/datasets/samuelcortinhas/house-price-prediction-seattle)**

It contains various features about houses, such as:
- Number of bedrooms and bathrooms,
- House size and lot size,
- Zip code, and
- Final sale price.

---

## 💻 Project Overview

The project workflow follows these main steps:
1. **Exploratory Data Analysis (EDA)**:
    - Data inspection, basic statistics, and plotting key relationships.
    - Detecting and handling missing values.
    - Unifying units of measurement (converting acres to square feet).

2. **Data Cleaning and Preprocessing**:
    - Dropping irrelevant columns (`zip_code`, `size_units`, `lot_size_units`).
    - Handling missing values (using median for `lot_size`).
    - Scaling numerical features using **StandardScaler**.

3. **Modeling and Evaluation**:
    - Training **Linear Regression**, **Ridge Regression**, and **Lasso Regression** models.
    - Cross-validation with grid search on regularization strength (`alpha`) for Ridge and Lasso.
    - Model performance evaluated with:
        - **Root Mean Squared Error (RMSE)**
        - **R² Score**

---

## 📊 Summary of Results

| Model | Test RMSE | Test R² Score |
|-------|-----------|---------------|
| Linear Regression | ✅ Best performance | ~53% variance explained |
| Ridge Regression | Slightly worse | Slight drop in performance |
| Lasso Regression | Similar to Ridge | No significant improvement |

- Linear Regression gave the best results in this setup.
- Regularization did not improve performance likely due to limited features and linear relationships.

---

## Future Improvements

- Incorporating more features (e.g., neighborhood, house condition).
- Trying non-linear models like Random Forest or Gradient Boosting.
- Applying feature engineering and log-transformations to improve performance.

---

## 📎 Repository Structure
├── Data/ # Dataset files
├── house_price_prediction // Main Notebook
├── README.md # Project overview and instructions
└── requirements.txt # Python dependencies


---

## ⚙️ Installation

To run this project:
```bash
git clone https://github.com/yourusername/house-price-prediction-seattle.git
cd house-price-prediction-seattle
pip install -r requirements.txt
jupyter notebook
```
