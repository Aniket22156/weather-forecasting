# Weather Data Analysis and Forecasting

## Overview

This project performs comprehensive **Exploratory Data Analysis (EDA)**, **Anomaly Detection**, and **Time Series Forecasting** on a global weather dataset. It applies various **machine learning and deep learning models** to predict temperature trends and evaluates their performance.

## Features

- **Anomaly Detection**: Identifies outliers in key weather parameters using Z-score analysis.
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
- **Jupyter Notebook / Google Colab**

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

- **ARIMA achieved the best performance** with the lowest MAE.
- **Prophet also performed well**, indicating strong time-series forecasting abilities.
- **Random Forest and XGBoost had moderate performance**.
- **SVR performed the worst**, indicating it struggles with time-dependent data.
- **LSTM had room for improvement** and may benefit from hyperparameter tuning.

## Future Improvements

- **Hyperparameter tuning for LSTM** to improve accuracy.
- **Hybrid models (e.g., ARIMA-LSTM)** for better predictive performance.
- **Incorporating external features** like atmospheric pressure, humidity, and wind speed.

## License

This project is licensed under the MIT License.

---

### Author

Developed by **Aniket Sharma**
