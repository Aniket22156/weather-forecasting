# Weather Data Analysis and Forecasting

## Overview

This project performs comprehensive **Exploratory Data Analysis (EDA)**, **Anomaly Detection**, and **Time Series Forecasting** on a global weather dataset. It applies various **machine learning and deep learning models** to predict temperature trends and evaluates their performance.

## Features

- **Anomaly Detection**: Identifies significant outliers in multiple weather parameters, helping refine the dataset.
- **Feature Engineering**: Adds lag variables and moving averages to enhance predictive models.
- **Time Series Forecasting**: Utilizes multiple models to predict temperature trends.
- **Model Comparison**: Evaluates different forecasting models using **Mean Absolute Error (MAE)**.

## Dataset

- **Source**: Google Drive
- **Path**: `/Dataset/Data/GlobalWeatherRepository.csv`
- **Key Variables**:
  - `temperature_celsius`
  - `wind_kph`
  - `pressure_mb`
  - `humidity`
  - `visibility_km`
  - `uv_index`
  - `air_quality_PM2.5`, `air_quality_PM10`

## Technologies Used

- **Python Libraries**: `pandas`, `numpy`, `seaborn`, `matplotlib`, `scipy`, `statsmodels`
- **Machine Learning Models**: `SVR`, `Random Forest`, `XGBoost`, `Prophet`, `ARIMA`
- **Deep Learning**: `LSTM (Keras/TensorFlow)`
- **Jupyter Notebook / Google Colab`

## Installation & Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/weather-forecasting.git
   cd weather-forecasting
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Mount Google Drive (if using Colab):
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```
4. Run the Python script or notebook.

## Model Performance

| Model         | MAE (Lower is better) |
| ------------- | --------------------- |
| **ARIMA**     | **3.0905**            |
| Prophet       | 3.1871                |
| Random Forest | 4.8502                |
| XGBoost       | 6.0818                |
| SVR           | 11.6189               |
| LSTM          | 5.1728                |

### Key Findings

- **ARIMA achieved the best performance**, with the lowest MAE (3.0905), making it the most accurate model for temperature forecasting.
- **Prophet followed closely behind**, demonstrating good forecasting capabilities.
- **Random Forest and XGBoost had moderate accuracy**.
- **SVR performed the worst**, struggling to capture temporal dependencies.
- **LSTM had a higher MAE than ARIMA and Prophet**, showing potential but needing further tuning.

## Climate and Environmental Insights

- Contrary to expectations, the **temperature trend appears to be decreasing**, suggesting potential short-term cooling effects or regional variations rather than a uniform warming trend.
- **Air quality and temperature have weak correlations**, indicating that other environmental factors (such as pollution sources and wind patterns) might have a stronger influence.
- **UV index and atmospheric pressure emerged as key predictors of temperature**, reinforcing the role of solar radiation and atmospheric dynamics.
- **Europe’s lower average temperature compared to other continents highlights the need for localized climate assessments rather than generalized global trends**.

## Future Improvements

- **Hyperparameter tuning for LSTM** to improve accuracy.
- **Hybrid models (e.g., ARIMA-LSTM)** for better predictive performance.
- **Incorporating external features** like atmospheric pressure, humidity, and wind speed.

## Conclusion

Based on our analysis and model comparison:

- **ARIMA outperformed all models** with the lowest MAE.
- **Prophet showed promising results**, making it a strong alternative.
- **Anomaly detection helped refine the dataset** by identifying significant outliers.
- **Feature engineering (lag features, moving averages) significantly improved predictions**.
- **Deep learning models like LSTM require further optimization** to compete with traditional statistical models.

Traditional statistical models like **ARIMA remain strong contenders** for time series forecasting. However, **deep learning approaches like LSTM have room for improvement** with proper tuning and feature engineering.

## License

This project is licensed under the MIT License.

---

### Author

Developed by **Aniket Sharma**
