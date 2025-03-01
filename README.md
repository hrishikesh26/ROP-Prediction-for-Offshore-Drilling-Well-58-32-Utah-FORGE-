# ROP Prediction for Offshore Drilling (Well 58-32 – Utah FORGE)

## Overview

This project develops a machine learning solution to predict the Rate of Penetration (ROP) in offshore drilling operations using 100k+ Pason log records from Well 58-32 (Utah FORGE). The model assists drilling engineers and power tool experts by providing accurate real-time predictions and enabling anomaly detection for proactive maintenance and operational optimization.

## Project Background

Offshore drilling requires precise monitoring of drilling parameters to ensure efficient and safe extraction of subsurface resources. The Utah FORGE dataset, collected during Phase 2B near Milford, Utah, contains detailed diagnostic data (e.g., ROP, weight on bit, temperature, pump pressure) that reflect both the performance of the drilling rig and the characteristics of the subsurface materials. This project leverages these data to predict ROP, a critical metric for drilling performance, and demonstrates the application of advanced machine learning techniques in the drilling and power tooling industries.

## Technical Approach

### Data Preprocessing & Feature Engineering
- **Robust Cleaning:** Removed infinite values and imputed missing values using median imputation.
- **Scaling & Transformation:** Applied robust scaling and log transformation to correct the heavy right skew of the ROP variable.

### Model Development
- **Supervised Learning:** Implemented a RandomForest regressor to predict ROP using multiple sensor inputs.
- **Hyperparameter Tuning:** Optimized the model via grid search with 5-fold cross-validation.
- **Model Evaluation:** Achieved test performance of MSE=0.037, MAE=0.107, and R²=0.919; visualized actual vs. predicted ROP and residuals across depth.

### Tools & Libraries
- **Language:** Python
- **Libraries:** pandas, NumPy, Matplotlib, scikit-learn
- **Dataset:** [Utah FORGE power tool and drilling data](https://gdr.openei.org/submissions/1113)
- **Environment:** Jupyter Notebook

## Domain Relevance

- **Drilling Optimization:** Enables real-time monitoring and adjustment of drilling parameters, reducing downtime and enhancing operational efficiency.
- **Anomaly Detection & Safety:** Detects drill bit failures or abnormal conditions through residual analysis, ensuring timely maintenance and increased safety.
- **Power Tool Integration:** Techniques are applicable to power tool data, providing a data-driven approach to improving performance and reliability in similar industrial settings.

