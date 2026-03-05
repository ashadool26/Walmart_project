# Walmart Weekly Sales Forecasting

A professional time-series forecasting project that analyzes Walmart store sales and predicts future weekly revenue using SARIMAX.

## Project Overview
This project uses historical Walmart weekly sales data to:
- analyze sales behavior at the store level,
- identify trend/seasonality patterns,
- compare yearly performance between stores, and
- forecast future sales for planning and decision-making.

The full workflow is implemented in **`Walmart_project.ipynb`**.

## Business Objective
Retail teams need reliable forecasts to support:
- inventory planning,
- staffing and operations,
- promotion timing, and
- revenue expectation management.

This notebook demonstrates a practical forecasting pipeline that can be adapted for any individual store in the Walmart dataset.

## Dataset
The notebook expects a CSV file named similar to **`Walmart DataSet.csv`** that includes at least:
- `Date`
- `Store`
- `Weekly_Sales`

## Methodology
The workflow follows these steps:

1. **Data loading and store-level filtering**
   - Reads the Walmart dataset from CSV.
   - Lets the user select a store ID.
   - Aggregates weekly sales by date for the selected store.

2. **Preprocessing**
   - Converts `Date` to proper `datetime` format.
   - Sets date as index for time-series modeling.

3. **Exploratory analysis**
   - Visualizes weekly sales trends.
   - Performs seasonal decomposition to inspect trend/seasonal/residual components.
   - Compares selected store performance against another store (example included for 2012).

4. **Modeling (SARIMAX)**
   - Builds a SARIMAX model using selected hyperparameters.
   - Fits the model on observed weekly sales.
   - Runs diagnostics to validate residual behavior.

5. **Forecast evaluation**
   - Generates one-step-ahead predictions.
   - Computes error metrics:
     - Mean Squared Error (MSE)
     - Root Mean Squared Error (RMSE)
   - Reviews residual magnitude.

6. **Future forecasting**
   - Produces a 12-week forward forecast.
   - Plots predicted values with confidence intervals.

## Tech Stack
- **Python**
- **Pandas / NumPy** for data manipulation
- **Matplotlib / Seaborn** for visualization
- **Statsmodels** for time-series decomposition and SARIMAX forecasting

## How to Run
1. Open `Walmart_project.ipynb` in Jupyter Notebook or Google Colab.
2. Update the CSV file path if needed.
3. Install dependencies (if not already installed):

```bash
pip install pandas numpy matplotlib seaborn statsmodels
```

4. Run notebook cells in order.
5. Provide a valid store ID when prompted.

## Key Deliverables
- Store-level sales trend visualizations
- Seasonal decomposition chart
- SARIMAX model summary and diagnostics
- Forecast performance metrics (MSE, RMSE)
- 12-week ahead sales forecast plot with confidence intervals

## Suggested Enhancements
- Add train/test split with cross-validation for time-series.
- Perform automated hyperparameter tuning.
- Include external regressors (holiday flags, fuel price, CPI, unemployment, promotions).
- Package notebook logic into reusable Python modules.
- Deploy as an API/dashboard for business users.

## Repository Structure
- `Walmart_project.ipynb` — end-to-end analysis and forecasting notebook.
- `README.md` — project documentation.

---
If you want, I can also provide:
- a **resume-ready project description**,
- a **short LinkedIn project summary**, and
- an **interview explanation script** for this project.
