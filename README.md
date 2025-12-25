# 📉 Customer Churn Prediction with Explainable AI

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![XGBoost](https://img.shields.io/badge/XGBoost-Model-green)
![SHAP](https://img.shields.io/badge/SHAP-Explainability-orange)

## 📌 Project Overview
Customer Churn is a critical metric in the telecommunications industry. This project builds a Machine Learning pipeline to predict which customers are likely to cancel their subscription. 

Unlike standard "Black Box" models, this project focuses on **Explainable AI (XAI)** using SHAP (Shapley Additive Explanations) to reveal the *root causes* of churn, empowering the business to take targeted retention actions.

## 🛠️ Tech Stack
* **Core:** Python, Pandas, NumPy
* **Machine Learning:** XGBoost (Extreme Gradient Boosting), Scikit-Learn
* **Explainability:** SHAP (Kernel Explainer with Custom Wrapper)
* **Visualization:** Matplotlib, Seaborn

## 📊 Key Results
| Metric | Score | Business Impact |
| :--- | :--- | :--- |
| **Accuracy** | **78%** | Reliable baseline prediction. |
| **Recall (Churn)** | **55%** | Successfully identifies >50% of at-risk customers before they leave. |

> **Note:** The model was optimized for **Recall** rather than just Accuracy, as missing a churning customer (False Negative) is more costly than a false alarm.

## 🔍 Top Business Insights
Based on the SHAP analysis, the top drivers of churn are:
1.  **Contract Type:** Customers on **Month-to-Month** contracts are highly likely to churn.
2.  **Internet Service:** Users with **Fiber Optic** service show higher dissatisfaction rates.
3.  **Payment Method:** Electronic Check users are more volatile than Credit Card users.

## ⚙️ Challenges & Solutions
**Challenge:** Version incompatibility between XGBoost 2.0+ and SHAP TreeExplainer caused the pipeline to crash.

**Solution:** Engineered a custom **"Bulletproof Wrapper"** function to bridge the two libraries. This wrapper intercepts the data, enforces float precision, and passes it safely to the model, ensuring 100% stability.

### 📊 Visualizing the Drivers (SHAP)
![SHAP Summary Plot](https://github.com/user-attachments/assets/10e85a51-e91b-48d3-8288-5728005d2b5c)

## 🚀 How to Run
1.  Clone the repository:
    ```bash
    git clone [https://github.com/Allan122/Customer-Churn-Prediction.git](https://github.com/Allan122/Customer-Churn-Prediction.git)
    ```
2.  Install dependencies:
    ```bash
    pip install pandas numpy xgboost shap scikit-learn matplotlib seaborn
    ```
3.  Run the Jupyter Notebook:
    ```bash
    jupyter notebook "Customer churn.ipynb"
    ```

## 👤 Author
**Allan Cheerakunnil Alex**
