# Datasheet for Demand Forecasting Model (Tuned Random Forest)

## 1. Motivation

**For what purpose was the dataset created?**  
The dataset was designed for a Kaggle competition, with the goal of forecasting daily sales over a 3-month horizon for 50 items across 10 stores. It provides a clean, structured environment to test time series forecasting techniques.

**Who created the dataset, and what is their relevant expertise?**  
Kaggle curated this dataset using simulated or anonymized retail data for the purpose of encouraging exploration of forecasting methods in a manageable setting.

**What is the target variable?**  
The target variable is `sales`, representing the number of items sold on each day per store-item combination.

---

## 2. Composition

**What does each instance (row) represent?**  
Each row represents the sales of a particular item in a particular store on a given date.

**How many instances are there?**  
The dataset contains over 900,000 rows covering 5 years of daily sales across 50 items and 10 stores.

**What features are included?**  
- `date`: Date of the transaction  
- `store`: Store ID  
- `item`: Item ID  
- `sales`: Target variable (units sold)  
- Engineered features: `lag_1`, `lag_7`, `lag_14`, `rolling_mean_7`, `rolling_std_7`, `day_of_week`, `month`, `year`, `is_weekend`, etc.

**Does the dataset contain missing values?**  
Missing values were introduced by lag features and removed prior to model training.

**Is the dataset anonymised or synthetic?**  
It is synthetic or anonymised and specifically curated for educational purposes.

---

## 3. Collection Process

**How was the data collected or generated?**  
Details are not explicitly provided, but the data appears to be either real retail data that has been anonymised or synthetically generated to mimic real-world patterns.

**Was the data manually cleaned or preprocessed?**  
Yes, minimal preprocessing was required. Lag features introduced nulls, which were removed, and temporal features were extracted from the date column.

---

## 4. Preprocessing

**What preprocessing was done before training?**  
- Lag and rolling statistics were calculated (e.g., `lag_1`, `rolling_mean_7`)  
- Temporal features (`day_of_week`, `is_weekend`, etc.) were extracted  
- Dataset was split into train and validation sets based on date  
- No scaling was applied since tree-based models were used  

---

## 5. Uses

**What are the intended uses of this model?**  
The model is intended to forecast daily sales for each store-item combination over the next 3 months. This can support inventory planning and demand forecasting in retail settings.

**What are the out-of-scope use cases?**  
- Price elasticity modelling  
- Forecasting at category level  
- Real-time forecasting without retraining

---

## 6. Distribution

**Is the dataset publicly available?**  
Yes, it is hosted on Kaggle:  
[https://www.kaggle.com/competitions/demand-forecasting-kernels-only](https://www.kaggle.com/competitions/demand-forecasting-kernels-only)

**Are there licenses or restrictions?**  
Use of the data is permitted under Kaggle’s competition rules and T&Cs. It is not to be used for commercial purposes.

---

## 7. Maintenance

**Will this dataset be updated?**  
Unlikely. The competition is static and intended for learning.

**Contact for dataset issues?**  
For any dataset-related questions, refer to the Kaggle discussion board associated with the competition.

---

## 8. Ethics and Bias

**Does the dataset reflect any societal bias?**  
No human attributes (e.g., gender, age, location) are included. However, as a synthetic dataset, it is not representative of all geographies or industries.

**Are there ethical concerns?**  
None observed, as the dataset is synthetic and does not contain personal or sensitive information.

---

## 9. Feedback and Contributions

**How can feedback be provided?**  
Issues or questions can be posted on the Kaggle competition forum.