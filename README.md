# Electric Power Project 🔌⚡

This repository contains a comprehensive data science pipeline for analyzing and forecasting household electricity consumption using both **supervised learning** and **unsupervised clustering techniques**. It was developed as a combined **Course Project** and **Project Work** for the Big Data Analytics and Text Mining course.

## 🔍 Project Overview

The project consists of two integrated parts:

### 1. Course Project – Supervised Forecasting
We predict the **average electricity consumption for the next 3 days** using historical data and engineered features.

**Algorithms used:**
- Random Forest
- Gradient Boosted Trees (GBT)
- Multilayer Perceptron (Keras)
- XGBoost
- LSTM with Time2Vec (Keras)

**Highlights:**
- 📈 After feature engineering (v3), XGBoost and MLP achieved **R² > 0.997** and **RMSE < 26 Wh**, indicating highly accurate short-term forecasts.
- LSTM with a Time2Vec-enhanced BiLSTM architecture also produced competitive performance.

### 2. Project Work – Clustering and Cluster-Specific Forecasting
We applied unsupervised clustering to reveal different consumption behavior patterns and built customized prediction models for each group.

**Techniques used:**
- KMeans and Hierarchical Clustering
- Dimensionality reduction with UMAP & t-SNE
- Per-cluster XGBoost regressors
- SHAP for model interpretability

**Results:**
- Cluster-wise models achieved **R² > 0.993** in all segments.
- Cluster-specific SHAP analysis revealed key drivers of consumption behavior (e.g., rolling statistics, lag features, voltage trends).



