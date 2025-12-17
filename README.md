# Software Defect Prediction Using LLMs

##  Overview
This project focuses on predicting software defects from textual bug reports using
contextual language model embeddings and machine learning classifiers.
The goal is to identify defective bug reports early by leveraging semantic
information present in bug descriptions.

---

##  Dataset
- Source: Eclipse Bug Repository
- Data Type: Textual bug reports with associated metadata
- Target Variable: `defective` (binary classification)

Key attributes include:
- Bug description
- Resolution status
- Priority and component information

---

##  Exploratory Data Analysis
Exploratory analysis reveals that resolution status is strongly associated with
defectiveness, with bugs marked as *FIXED* predominantly representing real defects.
However, resolution attributes are post-hoc in nature and may introduce label leakage.

Analysis of bug description length shows substantial overlap between defective and
non-defective cases, indicating that surface-level textual features alone are
insufficient for accurate prediction. These findings motivate the use of semantic
representations.

---

##  Methodology
1. Bug descriptions are transformed into dense vector representations using
   RoBERTa-based contextual embeddings.
2. The resulting embeddings are used as input to an XGBoost classifier.
3. Class imbalance is handled using weighted learning.
4. Model explainability is supported using SHAP-based analysis.

---

##  Evaluation Metrics
The model is evaluated using:
- Accuracy
- ROC-AUC Score
- Cross-Entropy Loss (Log Loss)
- Balanced Accuracy
- Matthews Correlation Coefficient (MCC)
- Brier Score Loss

---

##  Results
The proposed approach demonstrates strong predictive performance, highlighting
the effectiveness of combining semantic embeddings with robust classifiers for
software defect prediction.

---

##  How to Run
Open the notebook directly in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
(https://colab.research.google.com/github/Jasirdeen007/software-defect-prediction-llm/blob/main/software_defect_prediction_llm.ipynb)

---

##  License
This project is licensed under the MIT License.
