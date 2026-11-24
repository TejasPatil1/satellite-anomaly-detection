# satellite-anomaly-detection
an anomaly detector prediction system which shows you the health of satellite and potential upcoming threats towards satellites such as asteroids, wind storms ; On the bases of current situations  
# Satellite Anomaly Detection & Failure Prediction

## Problem Statement

Satellite systems continuously generate telemetry data containing information about their operational health.

Identifying abnormal behavior and anticipating potential equipment failures is important for maintaining mission reliability.

This project explores two Machine Learning approaches:

1. **Anomaly Detection:** Identifying unusual patterns in satellite telemetry.
2. **Failure Prediction:** Estimating the likelihood of potential equipment failures based on telemetry observations.

## Approach

The problem was divided into two independent Machine Learning tasks.

### 1. Anomaly Detection

**Algorithm:** Isolation Forest
**Learning Type:** Unsupervised Learning

Isolation Forest was selected to identify unusual telemetry observations without requiring labeled anomaly data.

The approach involves:

* Preparing multivariate telemetry observations.
* Training an Isolation Forest model on telemetry features.
* Identifying observations that deviate from learned patterns.
* Classifying observations as normal or anomalous.

### 2. Failure Prediction

**Algorithm:** XGBoost Classifier
**Learning Type:** Supervised Learning

XGBoost was selected to model relationships between telemetry parameters and failure-related patterns.

The approach involves:

* Preparing telemetry features and corresponding target labels.
* Training a gradient-boosted decision tree classifier.
* Learning relationships between operational parameters and failure outcomes.
* Generating failure probability estimates for new observations.

## Data

The project uses a combination of real-world reference datasets and synthetic telemetry.

**Data Sources:**

* NOAA :— Space weather observations.
* CelesTrak :— Satellite catalog and orbital information.
* Synthetic telemetry :- Generated observations for model development.

Synthetic telemetry was used to construct training observations for the ML models.

## Feature Categories

The models operate on satellite telemetry and operational indicators, including:

* Temperature measurements.
* Battery and power related parameters.
* Solar panel output.
* Fuel pressure.
* Thruster related measurements.
* Communication related parameters.

## Implementation

| Component           | Implementation |
| ------------------- | -------------- |
| Data Processing     | Pandas, NumPy  |
| Anomaly Detection   | Scikit-learn   |
| Failure Prediction  | XGBoost        |
| Model Serialization | Pickle         |
| Inference           | Python         |

## Key Concepts Applied

* Unsupervised Learning
* Supervised Classification
* Isolation-based Anomaly Detection
* Gradient Boosting
* Telemetry Feature Engineering
* Predictive Modeling
* Model Inference



## Future Scoope

* Time-series anomaly detection.
* Hyperparameter optimization.
* SHAP-based model explainability.
* Comparison with alternative anomaly detection algorithms.
* Evaluation on real satellite telemetry datasets.
* Temporal failure prediction.

---

**Domain:** Machine Learning 
( Currently integrated into (https://github.com/TejasPatil1/hack-orbit.git)
