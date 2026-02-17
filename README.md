# 🧬 Breast Cancer Detection using Serum miRNA: Replication & Innovation

This repository contains a comprehensive analysis, replication, and improvement of the study by **Shimomura et al. (2016)** published in *Cancer Science*: *"Novel combination of serum microRNA for detecting breast cancer in the early stage"*.

Using the **GSE73002** dataset (NCBI GEO), we successfully replicated the paper's findings and then improved upon them using modern Machine Learning techniques.

---

## 📌 Project Overview

We performed three distinct analyses:

### 1. Replication (Methodology Validation)
- **Goal:** To reproduce the exact Linear Discriminant Analysis (LDA) model described in the paper.
- **Method:** Recreated the specific training/test cohort split (Imbalanced Training: 74 Cancer / 1493 Control) as per Table 1 of the article.
- **Result:** Successfully replicated the high sensitivity (~97%) reported in the paper.

### 2. Verification (External Validation)
- **Goal:** To test the validity of the *exact diagnostic formula* published in the paper on the full raw dataset (N=4113).
- **Method:** Applied the published coefficients directly to the raw data (after internal control normalization).
- **Result:** Confirmed the diagnostic power of the 5-miRNA panel with an **AUC of ~0.95**.

### 3. Innovation (AI-Driven Discovery) 🚀
- **Goal:** To discover potentially *better* biomarkers using modern algorithms.
- **Method:** Used **Random Forest** for non-linear feature selection (on ~2500 genes) and **XGBoost** for classification.
- **Result:**
    - Discovered a **NEW set of 10 biomarkers** (distinct from the paper).
    - Achieved **Higher Specificity (95.6%)** compared to the paper (82.9%).
    - Achieved **Higher Accuracy (95.5%)** compared to the paper (89.7%).

---

## 📊 Results Summary

| Metric | Paper (2016) | Our Replication | **Our Innovation (XGBoost)** |
| :--- | :---: | :---: | :---: |
| **Accuracy** | 89.7% | 90.6% | **95.5%** 🏆 |
| **Sensitivity** | 97.3% | 82.4% | **95.3%** |
| **Specificity** | 82.9% | 98.1% | **95.6%** 🏆 |
| **AUC** | 0.971 | 0.940 | **0.978** |

> *Note: The Innovation model significantly reduces False Positives, making it a more robust screening tool.*

---

## 📂 Repository Structure
- `notebooks/`: Contains the Jupyter Notebooks with full code and outputs.
- `results/`: Saved plots (ROC Curves, Confusion Matrices).
- `data/`: Information about the dataset (GSE73002).

## 🛠️ Requirements
- Python 3.x
- pandas, numpy, matplotlib, seaborn
- scikit-learn
- xgboost

## 🔗 Reference
Shimomura, A. et al. "Novel combination of serum microRNA for detecting breast cancer in the early stage." *Cancer Science* 107.3 (2016): 326-334.
