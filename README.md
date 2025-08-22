## Enhancing Healthcare with AI: Transformer Models for Prediction in Maternal Health
📌 Introduction

Maternal mortality remains a critical public health issue in rural India, largely due to limited healthcare access and the absence of early warning systems. Traditional rule-based methods often lack real-time predictive capabilities.

This project explores explainable AI (XAI) to predict maternal health risks using demographic and clinical data. The focus is not only on prediction accuracy but also on interpretability using SHAP values to build trust among healthcare workers.

🎯 Objectives

Develop an explainable AI model for maternal health risk prediction.

Compare traditional ML models with deep learning (Tab-Transformer).

Use SHAP to interpret model predictions and enhance trust.

❓ Key Research Questions

Can deep learning outperform traditional ML in maternal risk prediction?

Which features are most predictive of maternal complications?

How does SHAP help in improving trust in AI-driven decisions?

🔬 Methodology
📂 Dataset

Source: Open Government Data Platform (India)

Size: ~30,000 records, 24 features

Features: Age, delivery history, awareness of HIV/RTI, awareness of danger signs, etc.

Target: outcome_pregnancy (3 classes → No risk, Cannot decide, Complication)

⚙️ Preprocessing

Missing values handled (imputation, column removal).

Categorical encoding (label encoding).

Class imbalance mitigated (stratified sampling).

🤖 Models Compared

Logistic Regression (baseline)

Random Forest (feature importance analysis)

Tab-Transformer (deep learning with self-attention for tabular data)

📊 Explainability

SHAP (SHapley Additive exPlanations) applied to all models for interpretability.

📈 Results
Model	Accuracy	F1-Score (Weighted)
Logistic Regression	84.58%	83.25%
Random Forest	85.96%	84.50%
Tab-Transformer	86.73%	N/A (best val. acc.)
🔑 Key Findings

Top Features: Age, delivery history, awareness of danger signs.

Tab-Transformer captured complex feature interactions better than traditional ML models.

SHAP revealed nonlinear relationships (e.g., age thresholds affecting risk).

📉 Visual Insights

Age Distribution: Younger mothers (<30) showed higher complication rates.

Feature Importance: Delivery history and maternal age were most influential.

⚡ Challenges & Solutions

Data Quality: Handled missing values and removed irrelevant features.

Class Imbalance: Addressed using stratified sampling.

Interpretability: SHAP provided actionable insights for healthcare workers.

🚀 Future Work

Expand to diverse regional datasets for better generalization.

Develop real-time deployment via mobile apps for rural health workers.

Explore hybrid models (Tab-Transformer + LSTM) for longitudinal data.

🌍 Impact

Clinical Utility: Enables early interventions with AI-driven risk stratification.

Trust & Explainability: SHAP builds confidence among non-technical healthcare providers.

Scalability: Random Forest provides a lightweight alternative for low-resource settings.

🛠️ Tech Stack

Python (Pandas, NumPy, Scikit-learn, PyTorch)

Deep Learning: Tab-Transformer

Explainability: SHAP

Visualization: Matplotlib, Seaborn
