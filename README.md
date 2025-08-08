# Air Quality and Health: A Data-Driven Analysis Using Machine Learning and Deep Learning

## 📌 Overview

This research-focused project investigates the impact of air quality on public health through comprehensive data analytics, lag-based statistical inference, and machine learning (ML) and deep learning (DL) methodologies. By integrating pollutant time series data with predictive modeling techniques, the project aims to identify patterns, forecast pollutant levels, and elucidate potential delayed health effects. This repository provides a pipeline from data preprocessing and exploratory data analysis (EDA) to advanced forecasting using LSTM networks.

---

## 🎯 Objectives

- To analyze trends, seasonality, and anomalies in key air pollutants.
- To assess lagged correlations between air pollutants and temporal behaviors.
- To implement and evaluate ML and DL models for pollutant forecasting.
- To identify pollutant-specific delay effects for informed environmental interventions.

---

## 📁 Dataset

**File:** `air_quality_pollutants_combined_dataset.csv`

This dataset consolidates hourly or daily observations of atmospheric pollutants and meteorological parameters. It includes:

- **Pollutants:** PM2.5, PM10, NO₂, black carbon, particulate matter, O₃
- **Temporal Coverage:** Multi-months data across seasonal cycles

The dataset has been cleaned, aligned, and imputed for missing values as part of the preprocessing pipeline.

---

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
