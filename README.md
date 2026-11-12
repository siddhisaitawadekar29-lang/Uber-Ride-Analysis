
# Uber Ride Analysis & Demand Forecasting
## 1. Project Overview
This project analyzes a synthetic Uber ride dataset (5,000 records from Jan 2025 to June 2025) to uncover ride patterns, peak demand hours, and pricing trends, followed by a Machine Learning model to forecast hourly ride demand.

## 2. Dataset & Preprocessing
- **Features:** Pickup/dropoff coordinates (latitude & longitude), `pickup_datetime`, `passenger_count`, and `fare_amount`.
- **Preprocessing:** Converted timestamps into datetime objects to extract `hour`, `day`, `month`, and `day_of_week`. Calculated trip distance (`distance_km`) using Euclidean distance formula. Checked for null values (0 missing values found).

## 3. Key Insights & Visualizations
- **Fare Trends:** Trip distance shows a strong positive correlation with `fare_amount`.
- **Peak Hours:** Ride distribution across 24 hours helps identify high-traffic windows for dynamic pricing and driver allocation.
- **Time-Series Trend:** Daily ride volume remains consistent across the 6-month window.

## 4. Machine Learning Model (Demand Forecasting)
- **Algorithm:** Random Forest Regressor (`scikit-learn`).
- **Results:** Achieved an RMSE of ~1.03 rides/hour and predicted hourly demand accurately.
