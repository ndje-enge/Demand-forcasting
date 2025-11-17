# Demand Forecasting Project

This project aims to apply time series techniques, notably the ARIMA model, to forecast demand using historical sales data from the Olist platform.

## Project Structure

- `demand_forcasting.ipynb`: Main notebook containing analysis, modeling, and visualizations.
- Data CSV files:
    - `olist_customers_dataset.csv`
    - `olist_orders_dataset.csv`


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

## Visualizations

### Customer Analysis

**Client Distribution per State**

![Client distribution per state](Visualizations/Client%20distribution%20per%20state.png)

**Client Distribution in Top 10 Cities**

![Client distribution in top 10 cities](Visualizations/Client%20distribution%20in%20top%2010%20cities.png)

**Unique and Repeated Clients**

![Unique and repeated clients](Visualizations/Unique%20and%20repeated%20clients.png)

### Time Series Analysis

**Sales per Day (without outliers)**

![Sales per day without outliers](Visualizations/Sales%20per%20day%20without%20outliers.png)

**ACF and PACF Analysis**

![ACF and PACF](Visualizations/ACF%20and%20PACF.png)

### Model Results

**Sales Forecast**

![Sales forcast](Visualizations/Sales%20forcast.png)

**Residuals of ARIMA Model**

![Residuals of ARIMA](Visualizations/Residuals%20of%20ARIMA.png)

## Requirements

- Python 3.9+
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `plotly`, `scikit-learn`, `statsmodels`, `pmdarima`, `kmodes`

## Usage

Open the `demand_forcasting.ipynb` notebook and run the cells in order to reproduce the analysis and modeling.

## Authors

Enge NOUADJE

Stive TEDOM 

Project completed during a summer break of the third year of ESILV engineering School in Data & IA major.
