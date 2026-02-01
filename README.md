#### HOME-LOAN-DEFAULT-
This project applies logistic regression to predict whether a borrower will default on a home loan. By analyzing borrower attributes (income, credit score, loan amount, employment status, etc.), the model estimates the probability of default.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 🏦 Home Loan Default Prediction
### *Targeting Financial Stability through Advanced ML*

<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=25&pause=1000&color=3F8CFF&center=false&vCenter=false&width=500&lines=Credit+Risk+Modeling;Star+Schema+Data+Integration;LightGBM+vs+Logistic+Regression;Precision+Banking+Analytics" alt="Typing SVG" /></a>

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=for-the-badge&logo=jupyter&logoColor=white)
![LightGBM](https://img.shields.io/badge/LightGBM-Performance-green?style=for-the-badge&logo=leaf&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

---

## 📖 Project Overview
Financial institutions need to accurately predict which customers will struggle to repay their loans. This project implements a **360-degree view** of the customer by integrating data from **7 internal and external sources** to predict loan default probabilities (Target 0 vs 1).

Unlike standard implementations that only use the main application file, this project utilizes **Advanced Feature Engineering** to aggregate behavioral history from credit bureaus and previous applications.

## 📊 The Challenge: 7-Table Relational Data
The complexity of this project lies in the data architecture. [cite_start]Information is spread across a relational schema with **One-to-Many** relationships [cite: 8-29]:

| Dataset | Description | Integration Strategy |
| :--- | :--- | :--- |
| **Application Train** | Main static application data (Target) | *Base Table* |
| **Bureau** | External credit history | Aggregated by `SK_ID_CURR` |
| **Bureau Balance** | Monthly balance of external credits | Aggregated by `SK_ID_BUREAU` -> Merged to Bureau |
| **Prev. Application** | History of previous internal loans | Aggregated (Mean/Max/Sum) |
| **Installments** | Payment history (Late/Missed) | **Critical Feature:** Calculated `Days_Late` before agg |
| **POS Cash** | Point-of-sale monthly balance | Aggregated by `SK_ID_CURR` |
| **Credit Card** | Credit card usage history | Aggregated by `SK_ID_CURR` |

---

## 🛠️ Tech Stack & Techniques
* **Language:** Python
* **Libraries:** `pandas`, `numpy`, `seaborn`, `matplotlib`, `scikit-learn`
* **Modeling:**
    * **LightGBM:** Selected for handling large-scale, missing, and non-linear data.
    * **Logistic Regression:** Used as a baseline for interpretability.
* **Techniques:**
    * **Star Schema Integration:** Merging 7 tables into one flat file.
    * **Class Weighting:** Handling the severe class imbalance (Target 0 >> Target 1).
    * **Median Imputation:** Filling missing values for linear baselines.

---

## 📈 Key Results
The project compared a linear baseline against a gradient boosting machine.

| Model | ROC-AUC Score | Key Takeaway |
| :--- | :--- | :--- |
| **Logistic Regression** | ~0.74 | Good baseline, but misses complex patterns. |
| **LightGBM** | **~0.77** | **Best Performer.** Successfully captures non-linear risk factors. |

> **Recommendation:** The LightGBM model is selected for production due to its superior ability to rank risky customers (higher AUC).

---

## 🏆 Challenges Solved
1.  **Data Fragmentation:** Used `groupby` aggregations (Mean, Max, Sum) to flatten one-to-many relationships (e.g., one user having 50 past payments) into single-row features.
2.  **Imbalanced Classes:** Applied `class_weight='balanced'` to force the model to prioritize detecting defaulters.
3.  **Missing Data:** Leveraged LightGBM's native handling of `NaN` values to preserve information in missing credit records.

---

## 🚀 How to Run
1.  Clone the repository.
2.  Install dependencies:
    ```bash
    pip install pandas numpy lightgbm scikit-learn matplotlib seaborn
    ```
3.  Ensure the dataset files (`application_train.csv`, `bureau.csv`, etc.) are in a folder named `dataset/`.
4.  Run the Jupyter Notebook:
    ```bash
    jupyter notebook Home_Loan_Default_Prediction.ipynb
    ```

---
*Created by Anwith J Kharvi and Team
