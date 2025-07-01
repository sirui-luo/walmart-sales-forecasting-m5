# Walmart Sales Forecasting

This project aims to predict the next 28-day unit sales of Walmart products using the M5 Forecasting dataset from Kaggle. We approach this as a time series forecasting challenge and evaluate both deep learning and tree-based models to capture temporal trends, seasonality, and promotional effects.

## Objective

The primary objective of this project is to accurately forecast the next 28-day unit sales for Walmart retail goods using the comprehensive M5 Forecasting [M5 Forecasting](https://www.kaggle.com/competitions/m5-forecasting-accuracy) dataset from Kaggle. 

This involves developing robust models capable of identifying and leveraging various time series components and external influences to provide reliable predictions for inventory management and supply chain optimization.

## Dataset
The M5 Forecasting - Accuracy dataset, provided by Walmart, is a rich and challenging time series dataset hosted on Kaggle. It contains:

* Hierarchical Sales Data: Unit sales for 3,049 products sold in 10 stores across 3 states (California, Texas, Wisconsin).

* Temporal Information: Daily sales data spanning from 2011 to 2016.

* Calendar Events: Information about holidays, special events (e.g., Super Bowl, Valentine's Day), and other relevant calendar details.

* Promotional Information: Details on price changes and promotional activities (e.g., "snap" sales events).

The dataset is particularly challenging due to its hierarchical nature, sparsity for new products, and complex interactions between various features.

## Methodology & Models Explored
This project evaluates a range of modeling techniques, encompassing both traditional machine learning and deep learning approaches, to tackle the nuances of the M5 dataset:

Feature Engineering: Extensive feature engineering was performed to extract valuable information from the raw data, including:

Lagged sales features

Rolling window statistics (mean, median, standard deviation)

Time-based features (day of week, day of month, week of year, month, year, etc.)

Categorical encoding for product, store, and state IDs

Incorporation of calendar event information (e.g., 'event_name_1', 'event_type_1')

Price-related features (e.g., sell_price, price differences)

Tree-Based Models:

LightGBM (LGBM): Known for its speed and efficiency on large datasets, LightGBM was extensively tuned and utilized due to its strong performance in past Kaggle forecasting competitions. It effectively handles categorical features and non-linear relationships.

(You could also mention if you tried XGBoost or CatBoost here, even if LGBM was the primary one)

Deep Learning Models:

Recurrent Neural Networks (RNNs) / LSTMs: Explored for their ability to capture sequential dependencies in time series data. (You can specify if you used a particular architecture, e.g., a stacked LSTM or GRU.)

Transformer Networks: Investigated the potential of Transformer architectures (or simplified versions) for long-range dependency capture in time series, given their success in natural language processing. (Only include if you genuinely explored them beyond a basic attempt).
