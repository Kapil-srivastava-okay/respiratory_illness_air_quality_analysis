# 🫁 Air Quality and Respiratory Health Analysis in the West Midlands (UK)

This project investigates the temporal relationship between atmospheric pollutants and respiratory health outcomes in the West Midlands, UK. Leveraging a 12-month dataset that merges government-sourced air quality and health data, the study applies time series analysis, statistical decomposition, and machine learning models to forecast acute respiratory illness (ARI) occurrences based on air pollutant exposure.

---

## 📌 Table of Contents

- [📊 Project Overview](#-project-overview)
- [📁 Dataset Description](#-dataset-description)
- [⚙️ Data Preprocessing](#️-data-preprocessing)
- [📈 Exploratory Data Analysis (EDA)](#-exploratory-data-analysis-eda)
- [🤖 Modeling Framework](#-modeling-framework)
- [📏 Evaluation Metrics](#-evaluation-metrics)
- [💻 Tech Stack](#-tech-stack)
- [📂 Repository Structure](#-repository-structure)
- [📌 How to Run](#-how-to-run)
- [📜 License](#-license)

---

## 📊 Project Overview

This study explores the relationship between air pollution and respiratory illness using a data-driven, reproducible methodology. Core aims:

- Analyze temporal patterns in air pollution and respiratory health
- Explore lagged relationships and seasonal trends
- Build predictive models to forecast ARI using pollutants

Models used include Random Forest, XGBoost, and LSTM with attention mechanisms.

---

## 📁 Dataset Description

**Time Span**: June 9, 2024 – June 8, 2025  
**Records**: 365 days  
**Variables**: 18 (1 date, 4 health indicators, 13 pollutant metrics)  
**Format**: Daily aggregated CSV

### 📍 Data Sources

- **Health Data**: UK Health Security Agency (UKHSA)
  - Acute Bronchiolitis Syndromic
  - Acute Respiratory Illness
  - Influenza-like Syndromic
  - Scarlet Fever Syndromic

- **Air Quality Data**: DEFRA Air Quality Archive
  - PM2.5, PM10, NO₂, NO, NOx, O₃, Black Carbon
  - Spectral Particulate Matter (UV, IR, Blue, Green, Red, Yellow)

---

## ⚙️ Data Preprocessing

Performed in Python using structured Jupyter Notebooks:

- Standardized date formats
- Imputed missing values using 7-day rolling mean
- Aggregated pollutants spatially across monitoring stations
- Merged datasets on the `date` field
- Final dataset validated for null values and consistency

---

## 📈 Exploratory Data Analysis (EDA)

- **Descriptive Statistics**: Mean, median, std, skewness
- **Time Series Visualization**: Raw and smoothed trends
- **Seasonal Decomposition**: STL decomposition (additive)
- **Correlation Analysis**: Pearson coefficients, heatmaps
- **Lag Analysis**:
  - Lag windows (1–14 days)
  - Cross-correlation functions
  - Almon lag models
- **AQI Proxy**: Custom seasonal overlay chart

---

## 🤖 Modeling Framework

### ✅ Models Implemented:

| Model                  | Description                                                                 |
|-----------------------|-----------------------------------------------------------------------------|
| Random Forest Regressor | Bagging-based ensemble; good for baseline performance                     |
| XGBoost (Tuned/Untuned) | Gradient boosting model with high predictive power                        |
| LSTM with Attention     | Sequence model capturing long-term temporal dependencies                  |

### 🔍 Rationale for Model Use:

- **Random Forest**: Robust to noise, interpretable, fast
- **XGBoost**: Accurate, handles feature interactions, feature importances via SHAP
- **LSTM**: Models sequences directly; highlights critical lag days

---

## 📏 Evaluation Metrics

To assess model performance on ARI prediction:

- **Mean Absolute Error (MAE)**
- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**
- **R² Score**
- **Feature Importance Analysis** (Tree-based models + SHAP values)

---

## 💻 Tech Stack

- **Language**: Python 3.x
- **Libraries**:
  - Data Processing: `pandas`, `numpy`
  - Visualization: `matplotlib`, `seaborn`, `plotly`
  - Time Series: `statsmodels`, `scipy`
  - Machine Learning: `sklearn`, `xgboost`
  - Deep Learning: `tensorflow`, `keras`
- **IDE**: Jupyter Notebooks
- **Version Control**: Git + GitHub

---

## 📂 Repository Structure



## 🧠 Project Structure

```bash
air_quality_health/
│
├── eda_air-quality.ipynb               # Exploratory data analysis
├── advanced_lag_analysis.ipynb         # Lag correlation & signal alignment
├── ml_dl_air_quality.ipynb             # ML and DL model implementation
├── LSTM.ipynb                          # LSTM forecasting model
├── air_quality_pollutants_combined_dataset.csv  # Preprocessed dataset
└── README.md                           # Project documentation
