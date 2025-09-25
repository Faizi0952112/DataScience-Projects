# Cab Fare Revenue Prediction using PySpark

This project uses **Apache Spark (PySpark)** to predict NYC taxi fares based on historical yellow cab trip data. It performs data preprocessing, feature engineering, and applies a linear regression model to predict the total trip fare.

---

## Dataset

The script expects a CSV file containing yellow taxi trip data with the following columns:
[Download Here](https://www.kaggle.com/datasets/diishasiing/revenue-for-cab-drivers)
- `tpep_pickup_datetime`
- `tpep_dropoff_datetime`
- `passenger_count`
- `trip_distance`
- `total_amount`

> Make sure your dataset contains headers and uses proper datetime formatting.

---

## Features Used

The following features are engineered from the dataset:

- `passenger_count` (number of passengers)
- `trip_distance` (distance of the trip in miles)
- `pickup_hour` (hour of day the ride started)
- `pickup_day` (day of week the ride started)
- `duration_minutes` (trip duration in minutes)

---

## Model

The model used is **Linear Regression** from PySpark’s MLlib.

- Feature vector is assembled using `VectorAssembler`.
- Model is trained on 80% of the data and evaluated on the remaining 20%.

### Evaluation Metrics:

- **RMSE (Root Mean Squared Error)**
- **R² Score (Coefficient of Determination)**

---

## How to Run

### 🛠 Requirements

- Python 3.x
- Apache Spark (with PySpark)
- Java 8+

### Run this in terminal:

```bash
spark-submit --master yarn --deploy-mode cluster <filePath> <dataSetPath> 

```
### 
