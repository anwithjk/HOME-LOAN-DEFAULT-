#### HOME-LOAN-DEFAULT-
This project applies logistic regression to predict whether a borrower will default on a home loan. By analyzing borrower attributes (income, credit score, loan amount, employment status, etc.), the model estimates the probability of default.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
<div align="center">

<img src="https://i.pinimg.com/originals/e0/94/2b/e0942b26058fa727e0255963f915764c.gif" width="100%" style="border-radius: 10px; box-shadow: 0px 0px 20px rgba(0, 255, 255, 0.5);" alt="Digital Evolution AI">

<br><br>

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.herokuapp.com?font=Orbitron&weight=900&size=35&pause=1000&color=00F0FF&center=true&vCenter=true&width=800&lines=HOME+LOAN+DEFAULT+PREDICTION;EVOLUTIONARY+DATA+SCIENCE;LIGHTGBM+|+XGBOOST+|+NEURAL+NETS;TARGETING+FINANCIAL+STABILITY" alt="Typing SVG" />
</a>

<p>
  <img src="https://img.shields.io/badge/CODE-PYTHON_3.8-00F0FF?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/DATA-STAR_SCHEMA-7000FF?style=for-the-badge&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/MODEL-LIGHTGBM-FF0055?style=for-the-badge&logo=google-cloud&logoColor=white" />
  <img src="https://img.shields.io/badge/STATUS-DEPLOYED-00FF99?style=for-the-badge&logo=github-actions&logoColor=black" />
</p>

<a href="https://d3ilbtxij3aepc.cloudfront.net/projects/CDS-Capstone-Projects/PRCP-1006-HomeLoanDef.zip">
  <img src="https://img.shields.io/badge/📥_DOWNLOAD_FULL_DATASET_(ZIP)-000000?style=for-the-badge&logo=dropbox&logoColor=00F0FF&labelColor=1a1a1a" />
</a>

</div>

---

## <img src="https://media.giphy.com/media/Wj7lNjMNDxSmc/giphy.gif" width="30"> Digital Project Architecture

**The Problem:** Financial institutions lose billions to loan defaults.
**The Evolution:** We replaced static analysis with a **dynamic, multi-table machine learning pipeline**.

<div align="center">
  <table align="center">
    <tr>
      <td align="center"><b>📂 INPUT DATA (The DNA)</b></td>
      <td align="center"><b>⚙️ PROCESSING (The Mutation)</b></td>
      <td align="center"><b>🧠 MODEL (The Intelligence)</b></td>
    </tr>
    <tr>
      <td align="center">7 Relational CSV Files<br>(Bureau, Payments, Apps)</td>
      <td align="center">Star-Schema Aggregation<br>Feature Flattening</td>
      <td align="center">LightGBM Gradient Boosting<br>ROC-AUC Optimization</td>
    </tr>
  </table>
</div>

---

## 📊 Performance Analytics

<div align="center">
  <img src="https://cdn.dribbble.com/users/1626229/screenshots/11252184/media/f470a27301c2069cb601d36802e3b26c.gif" width="700" alt="Data Analytics Animation" />
</div>

> **Verdict:** The evolutionary leap from Logistic Regression to **LightGBM** resulted in a **4.5% increase in ROC-AUC**, securing a "Production-Ready" status.

| Model Candidate | Score (AUC) | Speed | Intelligence Level |
| :--- | :--- | :--- | :--- |
| **Logistic Regression** | `0.741` | ⚡ Fast | 🟢 Basic (Linear) |
| **LightGBM** | **`0.775`** | 🚀 Moderate | 🟣 **Advanced (Non-Linear)** |

---

## 🛠️ The Tech Engine

<div align="center">
  <img src="https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white">
  <img src="https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white">
  <img src="https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white">
  <img src="https://img.shields.io/badge/LightGBM-%2332CD32.svg?style=for-the-badge&logo=leaf&logoColor=white">
</div>

### 🌪️ Challenges Overcome
* **Data Fragmentation:** Flattened 1-to-Many relationships using `groupby` aggregation.
* **Class Imbalance:** Utilized `class_weight='balanced'` to detect rare default events.
* **Missing Data:** Leveraged tree-based native handling of `NaN` values.

---

## 🚀 Initialize Sequence

```bash
# 1. Clone the repository
git clone [https://github.com/yourusername/home-loan-evolution.git](https://github.com/yourusername/home-loan-evolution.git)

# 2. Install High-Performance Libs
pip install lightgbm pandas scikit-learn matplotlib

# 3. Ignite the Kernel
jupyter notebook Home_Loan_Prediction.ipynb
