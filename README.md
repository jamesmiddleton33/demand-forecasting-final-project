# Final Project: Demand Forecasting for Retail Sales

## Project Overview

This project aims to predict future item-level sales across multiple stores using historical transactional data. The dataset, provided by Kaggle’s "Demand Forecasting - Kernels Only" competition, includes five years of daily sales data. The challenge is to forecast sales for the next three months for 50 unique items across 10 stores.

## Model Summary

A tuned **Random Forest Regressor** was selected as the final model after evaluating several machine learning approaches, including:
- **Linear Regression**
- **XGBoost**
- **LightGBM**

The Random Forest model was chosen based on its superior performance in RMSE and R² across both global and store-specific validation sets.

## Dataset

The dataset is not stored directly in this repository. You can access and download it from Kaggle:
[Demand Forecasting - Kernels Only Competition](https://www.kaggle.com/competitions/demand-forecasting-kernels-only)

After downloading, place the unzipped files in the `data/` directory.

## Repository Structure

```bash
├── data/                   # Contains raw and processed datasets (user must download from Kaggle)
├── notebooks/              # Jupyter Notebooks for EDA, modeling, and evaluation
├── reports/                # Documentation including model card and datasheet
├── model_card.md           # Documentation describing the final model
├── datasheet.md            # Description and context of the dataset
├── README.md               # Project overview and key results


