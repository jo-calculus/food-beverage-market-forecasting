# Food & Beverage Market Forecasting with ARIMA

A time-series analysis exploring historical trends and forecasting patterns across **food, beverage, consumer, and financial indicators** using ARIMA models.

The project covers time-series preparation, exploratory analysis, stationarity testing, model selection, forecasting, and evaluation.

## Overview

The goal of the analysis was to examine how selected market indicators changed over time and determine whether their historical behavior could be modeled using traditional statistical forecasting methods.

Rather than treating each series as ordinary tabular data, the project focuses on the characteristics that matter specifically for time series, including:

* long-term trends;
* temporal structure;
* stationarity;
* autocorrelation; and
* forecast error.

## Workflow

1. Data loading and inspection
2. Cleaning and preparation
3. Exploratory time-series visualization
4. Stationarity testing
5. Differencing where required
6. ACF and PACF analysis
7. ARIMA model specification
8. Forecast generation
9. Model evaluation using RMSE
10. Interpretation of forecast behavior

## ARIMA

The analysis uses **AutoRegressive Integrated Moving Average (ARIMA)** models.

An ARIMA model is represented as:

```text
ARIMA(p, d, q)
```

where:

* **p** represents autoregressive terms;
* **d** represents the degree of differencing used to achieve stationarity; and
* **q** represents moving-average terms.

Different combinations were evaluated depending on the behavior of each time series.

## Model Evaluation

Forecast performance was evaluated using **Root Mean Squared Error (RMSE)**:

$$
RMSE =
\sqrt{\frac{1}{n}
\sum_{i=1}^{n}
(y_i-\hat{y}_i)^2}
$$

Lower RMSE indicates that forecasts were, on average, closer to the observed values.

The notebook retains the model-specific results and plots from the original analysis.

## What the Project Demonstrates

This project focuses less on machine-learning complexity and more on the statistical reasoning required for forecasting.

It demonstrates:

* working with chronological rather than randomly shuffled data;
* identifying non-stationary behavior;
* applying transformations and differencing;
* interpreting ACF and PACF plots;
* fitting ARIMA models;
* evaluating forecasts against held-out observations; and
* communicating time-series behavior visually.

## Tools

`Python` `pandas` `NumPy`
`Matplotlib` `statsmodels`
`ARIMA` `ADF Test` `ACF` `PACF`

## Limitations

ARIMA relies primarily on the historical behavior of the series itself. It does not directly incorporate external variables such as policy changes, economic shocks, consumer sentiment, supply-chain disruptions, or other structural changes unless they are explicitly modeled.

The available historical period also limits how confidently long-range forecasts can be interpreted.

For a production forecasting system, this analysis could be extended with:

* SARIMA for seasonal patterns;
* ARIMAX/SARIMAX for external predictors;
* rolling-window validation;
* exponential-smoothing methods;
* Prophet or other structural time-series approaches; and
* machine-learning forecasting models for comparison.

## Notebook

➡️ [View the complete analysis](food_beverage_market_analysis_arima.ipynb)

## Data Availability

This project was originally completed as part of university coursework.

The original source datasets are no longer included in the repository. The notebook retains the outputs produced during the original execution so that the analytical workflow, visualizations, model results, and interpretation remain available.

---

*Academic time-series analysis reorganized for portfolio presentation.*
