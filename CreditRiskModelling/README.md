# Credit Risk Default Prediction Engine

## 📌 Project Overview
This project implements an end-to-end machine learning pipeline to assess credit risk for unsecured personal loans. The goal is to build a robust **Scorecard Model** that predicts the Probability of Default (PD) for loan applicants, aiding financial institutions in making data-driven lending decisions.

Unlike black-box models, this project utilizes **Weight of Evidence (WoE)** transformation and **Logistic Regression** to ensure high interpretability and regulatory compliance (Basel II/III standards).

## 🚀 Key Features
* **Robust Preprocessing:** Handling missing values and outliers using domain-specific capping and floor techniques.
* **Feature Engineering:** Implementation of **Weight of Evidence (WoE)** and **Information Value (IV)** to select predictive features while maintaining monotonicity.
* **Scorecard Development:** Transformation of model coefficients into a readable credit scorecard.
* **Model Performance:** Evaluated using AUC-ROC, Gini Coefficient, and Kolmogorov-Smirnov (KS) statistics.
* **Production Ready:** Deployed as a web application using **Flask** for real-time inference.

## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, SciPy
* **Web Framework:** Flask
* **Containerization:** (Optional: Add Docker if you use it later)

## 📂 Project Structure
This repository documents the entire lifecycle of the project, from initial data exploration to final deployment:

| Folder / File | Description |
| :--- | :--- |
| `01_Business_Understanding` | Initial analysis of the problem statement and dataset properties. |
| `02_EDA_and_Feature_Engineering` | Deep dive into data cleaning, univariate/bivariate analysis, and WoE transformation. |
| `03_Model_Training_Evaluation` | Model selection experiments, hyperparameter tuning, and performance metrics validation. |
| `04_Deployment_Setup` | Scripts and configurations for serving the model via API. |
| `src/` | Core source code for preprocessing pipelines and model utilities. |
| `app.py` | The main Flask application entry point. |

## 📊 Methodology
1.  **Data Ingestion:** Loaded historical loan data (2007-2014).
2.  **Target Definition:** Defined "Default" based on loan status (Charged Off, Default, Late 31-120 days).
3.  **Feature Selection:** Filtered features with low Information Value (IV < 0.02) and high multicollinearity.
4.  **Modeling:** Trained a Logistic Regression model on the WoE-transformed data.
5.  **Evaluation:**
    * **AUC-ROC:** 0.86 (Example value - update with yours)
    * **Gini:** 0.72 (Example value - update with yours)

## 💻 How to Run Locally

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/simrandhirwani/Credit-Risk-Project.git](https://github.com/simrandhirwani/Credit-Risk-Project.git)