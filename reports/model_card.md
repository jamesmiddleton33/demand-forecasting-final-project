# Model Card: Tuned Random Forest for Demand Forecasting
## Model Details
- Model Type: Random Forest Regressor
- Library: Scikit-learn
- Hyperparameter Tuning: RandomizedSearchCV
- Training Time: Approx. 20–30 minutes on MacBook (multi-core)
## Intended Use
This model is designed to forecast daily sales volume across 50 items and 10 stores for a 3-month future period, as part of a demand forecasting competition. It is intended for educational purposes and performance benchmarking.
## Model Architecture
- n_estimators: 150
- max_depth: None
- min_samples_split: 5
- min_samples_leaf: 4
- max_features: ‘sqrt’
## Dataset Information
- Source: Kaggle Competition: Demand Forecasting - Kernels Only
- Records: ~900,000 daily observations
- Features:
    - store, item (ID columns)
    - lag_1, lag_7, lag_14, lag_28
    - rolling_mean_7, rolling_mean_14, rolling_mean_30
    - rolling_std_7
    - day_of_week, month, year, is_weekend
## Evaluation Metrics
- Validation RMSE: 7.822
- Validation MAE: 6.015
- R² Score: 0.881
## Limitations
- Model does not account for price promotions or external market forces.
- Does not encode categorical features explicitly.
- Might underperform for items with irregular sales patterns.
## Ethical Considerations
- Forecast bias could affect downstream supply chain decisions.
- Accuracy per store may vary based on item diversity and sales volume.
