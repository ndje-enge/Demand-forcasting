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

This visualization shows the geographical distribution of customers across different Brazilian states. São Paulo (SP) has the highest concentration of customers, followed by Rio de Janeiro (RJ) and Minas Gerais (MG), reflecting the population density and economic activity in these regions.

**Client Distribution in Top 10 Cities**

![Client distribution in top 10 cities](Visualizations/Client%20distribution%20in%20top%2010%20cities.png)

This chart displays the top 10 cities with the highest number of customers. São Paulo dominates with significantly more customers than other cities, highlighting the importance of major urban centers in the e-commerce market.

**Unique and Repeated Clients**

![Unique and repeated clients](Visualizations/Unique%20and%20repeated%20clients.png)

This analysis distinguishes between unique customers (one-time buyers) and repeated customers (returning buyers). Understanding customer retention patterns is crucial for demand forecasting and business strategy.

### Time Series Analysis

**Sales per Day (without outliers)**

![Sales per day without outliers](Visualizations/Sales%20per%20day%20without%20outliers.png)

This time series plot shows the daily sales volume after removing outliers using the IQR method. The cleaned data reveals the underlying patterns and trends, making it more suitable for ARIMA modeling and ensuring more accurate forecasts.

**ACF and PACF Analysis**

![ACF and PACF](Visualizations/ACF%20and%20PACF.png)

The Autocorrelation Function (ACF) and Partial Autocorrelation Function (PACF) plots are essential for determining the appropriate parameters (p, d, q) for the ARIMA model. These plots help identify the order of autoregressive and moving average components in the time series.

### Model Results

**Sales Forecast**

![Sales forcast](Visualizations/Sales%20forcast.png)

This graph displays the ARIMA model's predictions overlaid with the actual historical sales data. The forecast line shows the expected future demand trends, allowing businesses to anticipate sales volumes and plan inventory accordingly.

**Residuals of ARIMA Model**

![Residuals of ARIMA](Visualizations/Residuals%20of%20ARIMA.png)

The residuals plot is crucial for evaluating model performance. Ideally, residuals should resemble white noise (random fluctuations around zero), indicating that the model has captured all systematic patterns in the data. This diagnostic helps validate the ARIMA model's adequacy.

## Requirements

- Python 3.9+
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `plotly`, `scikit-learn`, `statsmodels`, `pmdarima`, `kmodes`

## Usage

Open the `demand_forcasting.ipynb` notebook and run the cells in order to reproduce the analysis and modeling.

--

Project completed during a summer break of the first year of ESILV engineering School in Data & IA major.
