# Forecasting Mortgage Rates and Simulating Housing Prices Using ARIMAX

This project implements an ARIMAX model to forecast 30-year U.S. benchmark mortgage rates and simulate the resulting effects on housing prices under various Loan-to-Value (LTV) ratios. We aim to balance model flexibility with interpretability, using economic variables as external regressors in a time series context.

## 🔍 Motivation

Understanding the relationship between interest rates and housing markets is critical for mortgage risk assessment, homebuyer behavior, and macroeconomic planning. By forecasting long-term mortgage rates and simulating price effects under different leverage scenarios, we can better assess the sensitivity of housing markets to monetary policy shifts.

## 🧠 Model

The core model used is **ARIMAX (AutoRegressive Integrated Moving Average with eXogenous variables)**, implemented with:

- **Pmdarima**: for automated model selection and diagnostics
- **Statsmodels**: for transparent modeling and statistical inspection

### Features

- Target: 30-year fixed mortgage rates
- Exogenous regressors: macroeconomic indicators (e.g., CPI, Treasury yield, housing index)
- Simulated variable: housing prices under varying LTV scenarios (e.g., 60%, 80%, 95%)

### Workflow

1. Data preprocessing and alignment
2. Stationarity checks (ADF test)
3. Model selection with `auto_arima()`
4. Forecasting mortgage rates
5. Simulating housing price paths under different LTV regimes

## 📈 Results

- The ARIMAX model provided accurate short-horizon forecasts with interpretable coefficients.
- Housing price simulations showed significant sensitivity to the assumed LTV ratios.
  - Higher LTV settings amplified forecast variance and potential price volatility.
- Economic indicators (e.g., inflation, Treasury yields) had statistically significant influence on mortgage rates.

## 🧩 Dataset

While data is not publicly provided, typical sources used include:

- U.S. 30-Year Fixed Mortgage Rate (FRED)
- Consumer Price Index (CPI)
- U.S. Treasury 10-year Yield
- FHFA House Price Index

## 🧠 Reflection

This project deepened my understanding of dynamic time series modeling with external factors. ARIMAX provided a good compromise between transparency and performance, which is especially useful for financial forecasting tasks that require explainability. The simulation framework is extendable to stress testing and scenario analysis in real estate finance.

## 📌 Requirements

- Python 3.7+
- `pmdarima`
- `statsmodels`
- `pandas`, `numpy`, `matplotlib`

Install via:

```bash
pip install -r requirements.txt
