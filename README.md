Thyroid Cancer Risk Prediction Pipeline

Overview
This project implements a machine learning pipeline to predict thyroid cancer risk levels (Low, Intermediate, High) using the UCI Differentiated Thyroid Cancer Recurrence Dataset. Designed for clinical use, it combines high accuracy (91.67%) with interpretability through SHAP (SHapley Additive exPlanations) and includes a user-friendly command-line interface (CLI) for real-time risk predictions. The pipeline addresses research gaps in prior studies by providing explainable predictions and a practical deployment solution for oncologists.

Features
Data Preprocessing: Encodes categorical features (e.g., Gender, Smoking) using LabelEncoder and normalizes numerical features (Age) with MinMaxScaler.

Exploratory Data Analysis (EDA): Visualizes risk level distribution and feature correlations using Seaborn and Matplotlib.

Ensemble Model: Combines RandomForestClassifier and GradientBoostingClassifier with soft voting for robust predictions.

Model Evaluation: Achieves 91.67% accuracy and 0.88 macro F1-score, with a confusion matrix and 5-fold cross-validation.

Explainability: Uses SHAP to identify key features (e.g., Adenopathy, Tumor Stage, Nodal Stage) influencing predictions.

Command-Line Interface: Allows clinicians to input patient data and receive risk predictions with input validation.

Saved Artifacts: Stores encoders, scaler, model, and visualizations for reproducibility and deployment.


Dataset
Source: UCI Differentiated Thyroid Cancer Recurrence Dataset (DOI: 10.24432/C5632J).
Features: Includes Age, Gender, Smoking, Adenopathy, Tumor Stage (T), Nodal Stage (N), and more (excludes Response and Recurred).
Target: Risk level (Low, Intermediate, High).

Results
Model Performance:
Accuracy: 91.67%
Macro F1-score: 0.88
5-fold Cross-Validation F1-macro: 0.88 ± 0.03

Key Features (via SHAP):
Adenopathy, Tumor Stage (T), and Nodal Stage (N) are the most influential.
