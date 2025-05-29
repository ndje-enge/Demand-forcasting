# Demand Forecasting Project

This project aims to apply time series techniques, notably the ARIMA model, to forecast demand using historical sales data from the Olist platform.

## Project Structure

- `demand_forcasting.ipynb`: Main notebook containing analysis, modeling, and visualizations.
- Data CSV files:
    - `olist_customers_dataset.csv`
    - `olist_geolocation_dataset.csv`
    - `olist_order_items_dataset.csv`
    - `olist_order_payments_dataset.csv`
    - `olist_order_reviews_dataset.csv`
    - `olist_orders_dataset.csv`
    - `olist_products_dataset.csv`
    - `olist_sellers_dataset.csv`
    - `product_category_name_translation.csv`

## Main Steps

1. **Data Exploration and Cleaning**
     - Exploratory analysis of customers, orders, and sales.
     - Cleaning missing values and outliers (IQR method).
     - Aggregating sales by day.

2. **Time Series Analysis**
     - Visualization of daily sales.
     - ACF and PACF analysis to determine stationarity and ARIMA parameters.
     - Seasonal decomposition to identify trend and seasonality.

3. **Modeling**
     - Applying the ARIMA model (parameters determined via ACF/PACF).
     - Using `auto_arima` to optimize parameters.
     - Data normalization to improve model performance.

4. **Evaluation**
     - Residual analysis to check model adequacy (expecting white noise).
     - Interpretation of model metrics (`AIC`, `BIC`, coefficients, standard errors, log-likelihood).

5. **Limitations**
     - The dataset does not allow forecasting demand for a sufficiently long period (> 7 days).

## Results

- The ARIMA model was fitted to daily sales data.
- Model metrics (`AIC`, `BIC`, etc.) were analyzed to assess forecast quality.
- Residual diagnostics indicate whether the model fits the time series.

## Requirements

- Python 3.9+
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `plotly`, `scikit-learn`, `statsmodels`, `pmdarima`, `kmodes`

## Usage

Open the `demand_forcasting.ipynb` notebook and run the cells in order to reproduce the analysis and modeling.

## Authors

Project completed as part of a school assignment.
