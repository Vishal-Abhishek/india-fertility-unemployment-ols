# Female Unemployment and Fertility Dynamics in India: A Time-Series Econometric Analysis (1991–2023)

## Overview

This project estimates the impact of **female unemployment** on **fertility rates** in India while controlling for **urbanization** using a multiple linear regression framework.

---

## Model Specification

```text
Fertilityₜ = β₀ + β₁(Female Unemploymentₜ) + β₂(Urbanizationₜ) + εₜ
```

---

## Dataset

| | |
|---|---|
| **Source** | World Bank – World Development Indicators (WDI) |
| **Period** | 1991–2023 |
| **Frequency** | Annual |

---

## Variables

| | |
|---|---|
| **Dependent** | Fertility Rate |
| **Independent** | Female Unemployment Rate |
| **Control** | Urbanization Rate |

---

## Technical Workflow

- Imported World Bank time-series data using `readxl`.
- Renamed variables and standardized feature names for reproducibility.
- Performed missing value treatment using `na.omit()`.
- Conducted data quality checks and variable validation.
- Specified a multiple linear regression model using R's `lm()` function.
- Estimated model parameters using Ordinary Least Squares (OLS).
- Evaluated statistical significance through t-tests and p-values.
- Assessed overall model fit using R², Adjusted R², F-statistic, and Residual Standard Error.
- Interpreted regression coefficients as marginal effects while controlling for urbanization.
---

---

## Results

| Variable | Coefficient | p-value |
|-----------|------------:|---------:|
| Female Unemployment | -0.0896 | < 0.001 |
| Urbanization | -0.2034 | < 0.001 |

### Model Performance

| | |
|---|---|
| **R²** | 0.978 |
| **Residual Standard Error** | 0.0965 |

Both explanatory variables exhibit **statistically significant negative effects** on fertility at the **1% significance level**.
