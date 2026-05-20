# Bridge Sensor Data Analysis

End-to-end data science project analyzing structural bridge sensor data using machine learning and anomaly detection techniques.

## Project Overview

This project analyzes one year of hourly bridge sensor measurements from three bridges. The objective is to explore structural behavior patterns, predict structural strain, classify abnormal events, and detect anomalies using supervised and unsupervised machine learning methods.

The project includes:
- Exploratory Data Analysis (EDA)
- Regression Modeling
- Classification Modeling
- Anomaly Detection
- Engineering Interpretation

---

## Dataset

The dataset contains hourly sensor data from three bridges, including:

- Temperature
- Humidity
- Traffic count
- Truck count
- Wind speed
- Structural strain
- Vibration amplitude
- Tilt measurements
- Displacement
- Crack sensor readings
- Anomaly labels

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

---

## Exploratory Data Analysis

The EDA focused on:
- Time-series visualization
- Daily and weekly traffic patterns
- Correlation analysis
- Structural behavior analysis
- Relationship analysis between environmental and structural variables

Key observations:
- Structural variables such as vibration, tilt, and strain showed strong relationships.
- Traffic patterns followed expected daily and weekly cycles.
- Multiple sensor variables exhibited redundancy in describing structural behavior.

---

## Regression Modeling

Target variable:
- `strain_micro`

Models used:
- Linear Regression
- Random Forest Regressor

Evaluation metrics:
- MAE
- RMSE
- MAPE

### Results

| Model | MAE | RMSE | MAPE |
|---|---|---|---|
| Linear Regression | 4.17 | 5.28 | 2.89% |
| Random Forest | 3.42 | 4.43 | 2.89% |

Key findings:
- Random Forest slightly outperformed Linear Regression.
- Structural strain was largely predictable from sensor measurements.
- Feature importance analysis identified vibration, tilt, and strain as dominant predictors.

---

## Classification Modeling

Target variable:
- `anomaly`

Model used:
- Random Forest Classifier

Evaluation metrics:
- Accuracy
- Precision
- Recall
- ROC-AUC

### Results

- Accuracy: 99.94%
- Precision: 1.00
- Recall: 0.86
- ROC-AUC: ~1.00

Key findings:
- Vibration measurements dominated anomaly detection.
- Strong feature redundancy existed among structural variables.
- The dataset contained highly separable anomaly patterns.

---

## Anomaly Detection (Unsupervised Learning)

Model used:
- Isolation Forest

Objective:
- Detect anomalies without using labeled anomaly data during training.

Key findings:
- Isolation Forest identified unusual structural behavior patterns based solely on feature distributions.
- Unsupervised detection provides value when labeled anomaly data is unavailable.

---

## Engineering Interpretation

The analysis suggests that bridge anomalies are primarily reflected through dynamic structural behavior, particularly vibration and tilt measurements.

The project also demonstrates:
- Redundancy across sensor systems
- Strong relationships between structural response variables
- The importance of anomaly detection for infrastructure monitoring and predictive maintenance

---

## Correlation Heatmap

<img width="517" height="302" alt="image" src="https://github.com/user-attachments/assets/ebc01a46-2369-40c1-9cb6-9475d900631d" />

The correlation heatmap was used to identify linear relationships between environmental, traffic, and structural variables.

---

## Feature Importance

<img width="1245" height="622" alt="image" src="https://github.com/user-attachments/assets/b83e7d06-345d-47f8-b628-ee6bfb2416dd" />
Permutation feature importance was used to evaluate the true contribution of each feature to model performance.

---
## Future Improvements

Possible future extensions:
- Time-series forecasting models
- LSTM / deep learning approaches
- Real-time anomaly detection
- Sensor fusion methods
- Dashboard development using Power BI or Streamlit
