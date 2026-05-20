# Industrial_IoT_Fault_Detection_Dataset
Overview

This project implements a machine learning-based system to detect faults in industrial machines using IoT sensor data. The system analyzes real-time sensor readings such as vibration, temperature, pressure, and engineered features to classify machine health conditions.

The goal is to demonstrate how predictive maintenance can be achieved using basic machine learning techniques.

Dataset

The dataset contains 1000 samples with the following features:

Vibration (mm/s)
Temperature (°C)
Pressure (bar)
RMS Vibration
Mean Temperature
Fault Label (Target)

The dataset simulates industrial machine behavior under normal and faulty conditions.

Objective:
-> Predict machine health status (Normal or Faulty)
-> Analyze sensor behavior under different fault conditions
-> Identify important features contributing to faults
-> Build a basic predictive maintenance model
Machine Learning Workflow:
-> Data loading and preprocessing
-> Removal of unnecessary column (Timestamp)
-> Exploratory Data Analysis (EDA)
-> Feature-target split
-> Train-test split
Model training:
-> Logistic Regression
-> Random Forest Classifier
-> Model evaluation using:
-> Accuracy
-> Precision, Recall, F1-score
-> Feature importance analysis
Results:
-> Best Accuracy achieved: ~0.57
-> Random Forest performed better than Logistic Regression
-> Class imbalance affected minority fault detection
-> Model performs best on majority class (Normal condition)
Key Insights:
-> Sensor values show overlapping patterns between fault classes
-> Pressure, Temperature, and Vibration contribute differently to predictions
-> Class imbalance significantly affects model performance
-> Real-world industrial data is noisy and not perfectly separable
Feature Importance:

The model identified key contributors to fault detection:

-> Pressure (most influential in this dataset)
-> Temperature
-> Vibration
-> Engineered features (RMS Vibration, Mean Temp)
Limitations
-> Small dataset (1000 samples only)
-> Class imbalance present
-> No real-time streaming implementation
-> Basic ML models used (no deep learning or advanced tuning)
Future Improvements:
-> Apply SMOTE for class balancing
-> Use XGBoost for improved accuracy
-> Build real-time dashboard using Streamlit
-> Extend to time-series prediction (failure forecasting)
-> Deploy as IoT edge monitoring system
Tech Stack:
-> Python
-> Pandas
-> NumPy
Scikit-learn
Matplotlib
Seaborn
