# Business Analytics BSc Final Dissertation

**Project Title:**  
**Interpretable Deep Multimodal Prediction of 30-Day Readmissions in Elderly Patients Using Fine-Tuned ClinicalBERT and EHR Data**

This repository contains the full codebase for a final year dissertation exploring interpretable machine learning models that combine structured electronic health records (EHR) with clinical text data to predict 30-day hospital readmissions among elderly patients.

---

## Notebooks

### `Final_Preprocessing.ipynb`  
**Purpose:** Data cleaning, feature engineering, and structured model baselines.

**Key steps:**
- Mapping ICD codes, lab results, and prescriptions  
- Merging structured datasets  
- Aggregating to one row per admission  
- Calculating 30-day readmission outcome  
- Handling missing values and encoding features  
- SMOTEENN class balancing  
- Aligning patients with discharge notes  
- Training baseline models (Logistic Regression, Random Forest, XGBoost)

---

### `Final_Modelling_XAI_Dissertation.ipynb`  
**Purpose:** Fine-tuning ClinicalBERT and building multimodal deep learning models.

**Key steps:**
- Filtering notes for elderly patients  
- Chunking long discharge summaries  
- Fine-tuning ClinicalBERT using attention pooling  
- Extracting [CLS] embeddings  
- Training:
  - ClinicalBERT MLP  
  - Structured MLP  
  - Mid-fusion and Late-fusion models  
- Model interpretability with SHAP, Integrated Gradients, and attention gates

---

## Data Use Disclaimer  
This project uses the **MIMIC-IV** database, which is protected by a data use agreement.

- No raw MIMIC-IV data is included or shared.  
- All shared files are derived or tokenized outputs in full compliance with PhysioNet credentialed access requirements.

To access MIMIC-IV: [https://physionet.org](https://physionet.org)

---

## How to Reproduce

1. Obtain access to the MIMIC-IV dataset through PhysioNet.  
2. Run `Final_Preprocessing.ipynb` to prepare data.  
3. Run `Final_Modelling_XAI_Dissertation.ipynb` to fine-tune ClinicalBERT and train fusion models.  
4. Update all file paths to match your environment (e.g., Google Drive or local path).
