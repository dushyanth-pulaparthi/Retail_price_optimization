# 🛒 Retail Price Optimization Using XGBoost

This project uses machine learning (XGBoost Regression) to predict the **unit price** of a product in a retail setting based on historical sales data. The goal is to **optimize pricing** to maximize sales while maintaining profitability.

---

## 🔍 Problem Statement

In retail, setting the right price is crucial to maximizing revenue. Pricing a product too high can reduce sales volume, while pricing it too low can hurt margins.

This model attempts to:
- Learn the relationship between product features (e.g., category, date, quantity sold) and historical unit prices.
- Predict a unit price for new data inputs that likely maximizes total sales.

---

## 📁 Dataset

The dataset is a CSV file containing:
- Product category
- Order date
- Quantity sold
- Unit price (target variable)
- Other fields like total_price, product_id, etc.

**Note:** Redundant fields like `total_price`, `month_year`, and `product_id` are removed before training to reduce noise.

---

## 📊 Model Used

- **Algorithm**: [XGBoost Regressor](https://xgboost.readthedocs.io/)
- **Why XGBoost?**
  - Handles non-linear relationships well
  - Robust against overfitting with built-in regularization
  - Feature importance can be visualized

---

## 🧠 Workflow

1. **Data Cleaning**
   - Drop unnecessary columns
   - Encode categorical columns (e.g., product category)

2. **Model Training**
   - Split into training and testing sets (80/20)
   - Train an `XGBRegressor` with specified hyperparameters

3. **Model Evaluation**
   - RMSE and R² Score
   - Custom accuracy: predictions within ±10% of actual price

4. **Feature Importance**
   - Visualized using Seaborn barplot

5. **User Input Prediction**
   - After training, the script accepts user input for features
   - Predicts optimal unit price based on trained model

---

## 🧪 Example Usage

```bash
$ python retail_price_optimizer.py
