# Final Project: Demand Forecasting for Retail Sales

## Project Overview

This project aims to predict future item-level sales across multiple stores using historical transactional data. The dataset, provided by Kaggle’s "Demand Forecasting - Kernels Only" competition, includes five years of daily sales data. The challenge is to forecast sales for the next three months for 50 unique items across 10 stores.

## Model Summary

A tuned **Random Forest Regressor** was selected as the final model after evaluating several machine learning approaches, including:
- **Linear Regression**
- **XGBoost**
- **LightGBM**

The Random Forest model was chosen based on its superior performance in RMSE and R² across both global and store-specific validation sets.

## Repository Structure

```bash
├── data/                   # Contains raw and processed datasets
├── notebooks/              # Jupyter Notebooks for EDA, modeling, and evaluation
├── models/                 # Saved models and evaluation results
├── reports/                # Documentation including model card and datasheet
├── src/                    # Source code for feature engineering, training, etc.
├── model_card.md           # Documentation describing the final model
├── datasheet.md            # Description and context of the dataset
├── README.md               # Project overview and key results

