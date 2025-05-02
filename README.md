# Traffic-Prediction-Using-Sensor-Data
This project uses machine learning models (Random Forest and XGBoost Regressors) to predict traffic volume based on historical data and various weather-related features.

## 📁 Dataset

The dataset used is **Metro Interstate Traffic Volume**, which includes hourly data recorded from a traffic sensor on Interstate 94 in Minneapolis, Minnesota. It can be downloaded from [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Metro+Interstate+Traffic+Volume).

**File:** `Metro_Interstate_Traffic_Volume.csv`

## 📦 Required Libraries

Make sure to install the following libraries before running the code:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
```

## 🛠️ Features Engineering

The script performs the following preprocessing steps:

* Fills missing `holiday` values with `'None'`
* Converts `date_time` to Python datetime and extracts:

  * Hour
  * Day
  * Weekday
  * Month
  * Year
  * Weekend indicator
* Drops the original `date_time` column
* Applies one-hot encoding on categorical features: `holiday`, `weather_main`, and `weather_description`

## 🎯 Target Variable

* `traffic_volume`: Continuous variable indicating the traffic flow volume.

## 📊 Model Training

Two models are trained:

1. **Random Forest Regressor** (`sklearn`)
2. **XGBoost Regressor** (`xgboost`)

Both models are evaluated on:

* **MAE**: Mean Absolute Error
* **MSE**: Mean Squared Error
* **RMSE**: Root Mean Squared Error
* **R² Score**: Coefficient of Determination

## 🧪 Evaluation Metrics (Sample Output)

```
Random Forest Performance:
MAE: 203.41
MSE: 140773.56
RMSE: 375.20
R² Score: 0.9644

XGBoost Performance:
MAE: 225.61
MSE: 142941.28
RMSE: 378.08
R² Score: 0.9638
```

## 📈 Visualization 

To visualize feature importance, correlation heatmaps or prediction vs actual traffic volumes, you can add extra code using `matplotlib` or `seaborn`.
![image](https://github.com/user-attachments/assets/1e10129b-a79f-4ac1-961f-4e1e09b59757)


## 📌 Notes

* Ensure the CSV path in the code (`'/content/Metro_Interstate_Traffic_Volume.csv'`) is updated.
* The project is designed for a beginner to intermediate level understanding of regression and model evaluation.

## 📃 License

This project is for educational and research purposes.
