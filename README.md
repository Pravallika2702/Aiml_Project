

Market Sales Prediction using Random Forest

Project Overview:

This project predicts daily sales for multiple products using historical sales data and time-based features. The model uses Random Forest Regression to forecast sales, allowing businesses to optimize inventory, plan marketing campaigns, and make data-driven decisions.






Dataset :

File: market_sales.csv

Columns:

date: Date of the sales record

product_id: Unique identifier for each product

sales: Number of units sold

The dataset contains historical sales data for multiple products over time.






Features :

The following features are generated for model training:

Time-based features

year, month, day, weekday

is_weekend: Binary flag for weekends

month_sin, month_cos: Cyclical encoding of months to capture seasonality

Lag features (to capture sales trends)

lag_1: Sales of the previous day

lag_7: Sales of 7 days ago

lag_14: Sales of 14 days ago





Product encoding :

product_id is one-hot encoded to handle categorical values





Model :

Algorithm: Random Forest Regressor

Hyperparameters:

n_estimators=400

max_depth=10

min_samples_split=2

min_samples_leaf=1

random_state=42

n_jobs=-1 (parallel computation)

Trained using an 80/20 train-test split.







Performance Metrics :

After training, the model is evaluated using:

MAE (Mean Absolute Error)

RMSE (Root Mean Squared Error)

R² Score (Coefficient of Determination)

The metrics are printed in the console after execution.






Visualization :

Actual vs Predicted Sales

The first 150 time steps of actual and predicted sales are plotted for visual comparison.







Requirements :

Python 3.8+

Libraries:

pandas

numpy

matplotlib

scikit-learn






Usage (Google Colab) :

-> Open Google Colab: https://colab.research.google.com

1.Upload your notebook sales_prediction.ipynb to Colab or open it directly from GitHub.

2.Upload the dataset market_sales.csv to Colab:

  1.Click the folder icon on the left panel
  
  2.Click the upload icon and select market_sales.csv
  
3.Run the cells sequentially. The notebook will:

  1.Load and preprocess the dataset 
  
  2.Train the Random Forest model
  
  3.Output evaluation metrics (MAE, RMSE, R²)
  
  4.Plot Actual vs Predicted sales
  





 
Output: 

The script will output model evaluation metrics and a plot of actual vs predicted sales.
