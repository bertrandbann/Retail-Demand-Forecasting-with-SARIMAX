# Retail-Demand-Forecasting-with-SARIMAX
🛒 Retail Demand Forecasting with SARIMAX
📌 Business Context

Retailers must decide how much stock to hold and when to reorder in an environment shaped by promotions, price changes, seasonality, and customer behaviour. Poor forecasts lead to either stock-outs (lost sales) or excess inventory (cash tied up and waste).

Traditional forecasting approaches that rely only on past sales often fail during promotions, seasonal peaks, and competitive price changes. This project demonstrates how data-driven demand forecasting can be used to support inventory, promotion, and cash-flow decisions.

🎯 Objective

The objective of this project is to build a robust retail demand forecasting model that:

Predicts future demand

Accounts for pricing, discounts, competitor pricing, seasonality, region, and product mix

Captures repeating demand cycles common in retail operations

This enables the business to move from reactive reporting to proactive inventory and revenue planning.

🔍 Methodology

Demand aggregation
Daily demand was aggregated across all stores and product categories to create a time series suitable for forecasting.

Stationarity testing
The Augmented Dickey–Fuller (ADF) test was used to confirm that the demand series was stationary, making it suitable for ARIMA-based models.

Seasonality detection
ACF and PACF analysis revealed a 10-day demand cycle, indicating a repeating retail rhythm (e.g., replenishment or promotion cadence).

Business drivers
The model incorporates key demand drivers:

Price

Discount / promotion

Competitor pricing

Product category mix

Regional demand mix

Seasonality and weather

Categorical variables were converted into dummy variables using one-hot encoding.

Forecasting model
A SARIMAX (Seasonal ARIMA with exogenous variables) model was built to capture both:

The 10-day demand cycle

The impact of business and market variables

Model validation
Residual diagnostics (Ljung-Box, Jarque-Bera, heteroskedasticity tests) confirmed that the model errors behave like white noise, indicating a statistically reliable forecast.

📊 Key Business Insights

The model shows that:

Promotions and discounts significantly increase demand

Competitor price changes directly affect sales volume

Demand follows a 10-day operational cycle, consistent with retail replenishment and promotion patterns

Toys and groceries are the most volatile categories, requiring tighter stock control

Regional demand differences are substantial, meaning inventory should not be allocated uniformly

🧠 Business Value

This forecasting framework can be used to support:

Inventory planning – when and how much to reorder

Promotion strategy – anticipating demand spikes

Cash-flow forecasting – reducing over-stocking

Regional stock allocation – matching supply to demand patterns

By integrating time-series dynamics with commercial drivers, the model provides a decision-support tool rather than a simple forecast.

🛠 Tools & Technologies

Python

pandas, NumPy

statsmodels (SARIMAX, ADF test, ACF/PACF)

Matplotlib / Seaborn
