# TabFGT-GRAFTS

This repository contains the experimental codes for **GRAFTS + TabFGT**, an interpretable machine learning framework for early lung cancer risk prediction using tabular clinical and lifestyle features. The framework combines **GRAFTS**, a graph-based feature-selection strategy, with **TabFGT**, a token-based feature-gated transformer for tabular classification.

The experiments include main model training, baseline comparison, feature-selection comparison, ablation study, calibration analysis, explainability analysis, and external/cross-dataset validation.

---

## Short Description

The project focuses on lung cancer risk prediction from tabular data. GRAFTS selects stable and informative features using graph-based evidence, role consistency, and redundancy control. TabFGT then performs classification using feature-preserving tokenization, feature-gated contextual encoding, and dual-view readout. The framework is evaluated using test-set metrics, nested cross-validation, calibration, explainable AI methods, and external validation datasets.

---

## Repository Files

| File | Description |
|---|---|
| `Main_GRAFTS_TabFGT.ipynb` | Main notebook for running the proposed GRAFTS + TabFGT framework on the primary lung cancer dataset. |
| `Baseline_Study.ipynb` | Compares TabFGT with baseline models such as GaussianNB, ExtraTrees, RandomForest, MLP-based models, SAINT, AutoInt, and TabTransformer. |
| `feature_selection_comparsion.ipynb` | Compares GRAFTS with other feature-selection methods such as ANOVA and related standard selectors. |
| `Ablation_Study_GRAFTS_TabFGT.ipynb` | Performs ablation experiments to evaluate the contribution of GRAFTS and TabFGT components. |
| `xai_and_calibration.ipynb` | Generates explainability and calibration results, including SHAP, LIME, PDP/ICE, ALE, Brier score, and calibration plots. |
| `External_Validation_Lung_cancer.ipynb` | Performs external validation using an additional lung cancer-related dataset. |
| `Cross_Dataset_Breast_Cancer.ipynb` | Evaluates cross-dataset generalization on a breast cancer dataset. |
| `Cross_Dataset_Kidney_Disease.ipynb` | Evaluates cross-dataset generalization on a chronic kidney disease dataset. |

---

## Datasets

### Primary Dataset

**Lung Cancer Prediction Dataset**  
https://www.selectdataset.com/dataset/e466a8895bac9e058f1182103f078688

This dataset contains 5,000 records and 30 features, including demographic, smoking-related, clinical, and lifestyle factors. The target variable is binary and represents lung cancer risk.

### External and Cross-Dataset Validation Data

The following datasets were used for external and cross-dataset validation:

- Breast Cancer Dataset:  
  https://www.kaggle.com/datasets/adhamelkomy/breast-cancer/data

- Chronic Kidney Disease Dataset:  
  https://doi.org/10.24432/C5G020

- Cancer Patients and Air Pollution Dataset:  
  https://www.kaggle.com/datasets/thedevastator/cancer-patients-and-air-pollution-a-new-link

---

## Method Overview

The proposed framework contains two main parts:

1. **GRAFTS Feature Selection**
   - Builds feature relationships using graph-based evidence.
   - Measures feature stability, role consistency, and redundancy.
   - Selects a compact and informative feature subset.

2. **TabFGT Classification Model**
   - Uses Feature-Preserving Tokenization.
   - Applies Feature-Gated Contextual Encoding.
   - Uses Dual-View Readout for final prediction.

---
