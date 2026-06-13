# Breast Cancer Classification using Machine Learning

## 📌 Project Overview
This project applies machine learning techniques to predict whether a breast tumor is malignant or benign based on digitized cellular measurements. Built using Python and `scikit-learn`, it serves as a practical implementation of binary classification, model evaluation, and feature importance analysis. 

This repository was developed as part of a portfolio for the **Amazon ML School**.

## 📊 The Dataset
The model is trained on the **Breast Cancer Wisconsin (Diagnostic) Dataset**, originally collected at the University of Wisconsin Hospitals and accessed via the UCI Machine Learning Repository.
* **Instances:** 569 patient records
* **Features:** 30 numeric predictive attributes (e.g., mean radius, texture, perimeter, area, smoothness, compactness)
* **Classes:** 
  * `0` - Malignant (Cancerous)
  * `1` - Benign (Healthy)

## 🛠️ Methodology & Tech Stack
* **Language:** Python 3
* **Environment:** Google Colab
* **Libraries:** `pandas`, `scikit-learn`, `matplotlib`
* **Algorithm:** Random Forest Classifier (`n_estimators=100`)
* **Process:** 
  1. Loaded and structured the raw data.
  2. Performed an 80/20 Train-Test split to ensure the model was evaluated on unseen data.
  3. Trained a Random Forest ensemble model.
  4. Generated confusion matrices and extracted feature importance scores to interpret model behavior.

## 🚀 Model Performance
The Random Forest model demonstrated high reliability in distinguishing between benign and malignant cases.

* **Overall Accuracy:** **96.49%**
* **Weighted F1-Score:** **0.96**

**Class-Specific Metrics:**
| Target Class | Precision | Recall | F1-Score |
| :--- | :--- | :--- | :--- |
| **Malignant (0)** | 0.98 | 0.93 | 0.95 |
| **Benign (1)** | 0.96 | 0.99 | 0.97 |

## 💡 Key Learnings & Takeaways
* **Medical Context:** In medical diagnostics, *Recall* for malignant cases is critical. While the model achieves 99% recall for benign cases, the 93% recall for malignant cases highlights the trade-off between minimizing false positives and false negatives.
* **Feature Importance:** Visualizing the Random Forest decision process revealed that features relating to the "worst" dimensions of the tumor (e.g., worst area, worst perimeter) carry the highest predictive weight.

## 🔮 Future Scope
* **Web Integration:** Serve the model via a REST API (using Node.js/Express) and integrate it into a full-stack React frontend to allow users to input parameters and receive real-time predictions.
* **Hyperparameter Tuning:** Implement `GridSearchCV` to optimize the Random Forest's depth and estimators to push the malignant recall score higher.

---
**Author:** Kunal More
