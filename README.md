# Dissertation
Business Analytics Bsc Final Dissertation

ClinicalBERT Fusion Models for 30-Day Readmission Prediction
This repository contains the full codebase for the final year project titled:
“Interpretable Deep Multimodal Prediction of 30-Day Readmissions in Elderly Patients Using Fine-Tuned ClinicalBERT and EHR Data”

Notebooks
Final_Preprocessing.ipynb
Purpose: Data cleaning, feature engineering, and dataset preparation.
Key steps:

Mapping diagnoses, procedures, labs, prescriptions

Merging structured data sources (ICD, labs, meds)

Aggregating long-format data into one row per admission

Calculating readmission target variable

Imputation and encoding

SMOTEENN resampling

Aligning patients with clinical notes

Traditional baseline models (LR, RF, XGBoost)

Final_Modelling_XAI_Dissertation.ipynb
Purpose: Fine-tuning ClinicalBERT, extracting attention-based embeddings, and implementing hybrid models.
Key steps:

Loading and filtering discharge notes by elderly cohort

Sliding window chunking and ClinicalBERT fine-tuning

Attention pooling and [CLS] embedding extraction

Structured MLP, ClinicalBERT MLP, and Mid-/Late-Fusion models

SHAP, Integrated Gradients, and attention gate analysis

Data Use Disclaimer
This project uses the MIMIC-IV database, which is protected under a data use agreement.
No raw MIMIC-IV data is included or shared.
All outputs are limited to derived features and minimal processed subsets (e.g., tokenized embeddings), in full compliance with the credentialed access terms.
Please refer to https://physionet.org to request access.

How to Reproduce
Due to licensing restrictions, users must have access to MIMIC-IV. Once access is granted:

Preprocess data using Final_Preprocessing.ipynb

Train and evaluate models using Final_Modelling_XAI_Dissertation.ipynb

Adjust paths in code cells to match your local or Google Drive file structure
