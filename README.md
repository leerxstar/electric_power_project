# ⚡ Electric Power Consumption Forecasting & Pattern Mining

## 📂 Dataset: Individual Household Electric Power Consumption  
**Link**: [UCI Repository](https://archive.ics.uci.edu/ml/datasets/individual+household+electric+power+consumption)

This dataset records minute-level electricity usage from a single household over nearly four years (Dec 2006 – Nov 2010). After preprocessing and aggregation to daily granularity, the final dataset includes:

- ~2,075,259 total observations  
- 9 continuous numeric features (voltage, active/reactive power, sub-metering, etc.)
- Derived temporal & statistical features for modeling and clustering  
- ≈ 18 million total data points (N × p)

---

## 🚀 Project Overview

This unified project integrates **two major components**:
- **Course Project**: Supervised electricity demand forecasting and anomaly-aware model refinement  
- **Project Work**: Unsupervised pattern discovery and cluster-specific forecasting with explainable modeling

### 🎯 Key Goals:
- Predict 3-day average electricity consumption from historical trends  
- Identify usage behavior patterns using clustering + dimensionality reduction  
- Build interpretable, cluster-aware predictive models using SHAP  

---

## 🔧 Technical Summary

| Task                        | Methodologies Used                                                                 |
|-----------------------------|------------------------------------------------------------------------------------|
| Supervised Regression       | Random Forest, GBT, MLP (Keras), LSTM, XGBoost                                    |
| Unsupervised Clustering     | KMeans, Agglomerative Clustering                                                  |
| Dimensionality Reduction    | UMAP, t-SNE                                                                       |
| Anomaly Detection           | Z-Score, Isolation Forest                                                         |
| Time Series Decomposition   | Seasonal-Trend Analysis (weekly)                                                 |
| Explainability              | SHAP (per-cluster)                                                                |

---

## 📈 Project Highlights

### ✅ Best Model Performance (Global)
Using enhanced time-series features & anomaly filtering:

| Model      | RMSE    | MAE     | R²     | NRMSE  |
|------------|---------|---------|--------|--------|
| **MLP**    | 23.02   | 15.77   | 0.9979 | 0.0082 |
| **XGBoost**| 25.26   | 14.21   | 0.9974 | 0.0090 |

### 🧠 Cluster-Specific Modeling (XGBoost Per Cluster)
By segmenting data into behavior-based clusters and training separate models:

- Cluster 0: R² = 0.995, NRMSE = 0.0149  
- Cluster 1: R² = 0.993, NRMSE = 0.0164  

**Result**: Improved interpretability and local accuracy over global models.

### 🔍 Feature Importance Analysis
SHAP analysis provided interpretable insights into dominant predictors per cluster—e.g., previous-day consumption, rolling means, and voltage-related metrics—revealing behavioral distinctions across user segments.

---

## 🧪 Technical Stack

Details in the requirements.txt

- **Language**: Python (3.10)  
- **Environment**: Conda (`bigdata_project`), Jupyter Notebook  
- **Cluster**: Local Spark 3.1.1 (Hadoop 2.7) with OpenJDK 17  
- **ML Libraries**: scikit-learn, XGBoost, TensorFlow (Keras), PySpark MLlib  
- **EDA & Viz**: matplotlib, seaborn  
- **Model Interpretation**: SHAP  
- **Dimensionality Reduction**: UMAP, t-SNE  
- **Time Series Tools**: statsmodels, pandas  







