# Market Sales Prediction using Random Forest

## Project Overview
This project predicts daily sales for multiple products using historical sales data and time-based features. The model uses **Random Forest Regression** to forecast sales, allowing businesses to optimize inventory, plan marketing campaigns, and make data-driven decisions.

---

## Dataset

**File:** `market_sales.csv`  

**Columns:**
- `date` — Date of the sales record  
- `product_id` — Unique identifier for each product  
- `sales` — Number of units sold  

The dataset contains historical sales data for multiple products over time.  

**Download Link:** [Market Sales Forecasting Dataset on Kaggle](https://www.kaggle.com/datasets/sahideseker/market-sales-forecasting-dataset?utm_source=chatgpt.com)  



---

## Features

### Time-Based Features
- `year`, `month`, `day`, `weekday`  
- `is_weekend` — Binary flag for weekends  
- `month_sin`, `month_cos` — Cyclical encoding of months to capture seasonality  

### Lag Features (to capture sales trends)
- `lag_1` — Sales of the previous day  
- `lag_7` — Sales of 7 days ago  
- `lag_14` — Sales of 14 days ago  

### Product Encoding
- `product_id` is **one-hot encoded** to handle categorical values

---

## Model

**Algorithm:** Random Forest Regressor  

**Hyperparameters:**
- `n_estimators = 400`  
- `max_depth = 10`  
- `min_samples_split = 2`  
- `min_samples_leaf = 1`  
- `random_state = 42`  
- `n_jobs = -1` (parallel computation)

**Training:** 80/20 train-test split

---

## Performance Metrics

The model is evaluated using:  
- **MAE (Mean Absolute Error)**  
- **RMSE (Root Mean Squared Error)**  
- **R² Score (Coefficient of Determination)**  

Metrics are printed in the console after training.

---

## Visualization

A plot is generated to compare **Actual vs Predicted Sales** for the first 150 time steps, helping visualize model performance.

---

## Requirements

- **Python 3.8+**  
- **Libraries:**  
  - `pandas`  
  - `numpy`  
  - `matplotlib`  
  - `scikit-learn`  

---

## Usage (Google Colab)

1. Open [Google Colab](https://colab.research.google.com)  
2. Upload your notebook `sales_prediction.ipynb` to Colab or open it directly from GitHub.  
3. Upload the dataset `market_sales.csv`:
   - Click the **folder icon** on the left panel  
   - Click the **upload icon** and select `market_sales.csv`  
4. Run the notebook sequentially. It will:
   1. Load and preprocess the dataset  
   2. Train the Random Forest model  
   3. Output evaluation metrics (MAE, RMSE, R²)  
   4. Plot Actual vs Predicted sales  

---

## Output

The notebook outputs:  
- Model evaluation metrics in the console  
- Plot of **Actual vs Predicted Sales** for visual comparison

