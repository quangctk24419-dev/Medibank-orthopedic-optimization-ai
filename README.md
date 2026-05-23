# 🏥 Medibank Orthopedic Optimization: AI-Driven Clinical & Financial Strategy

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Machine Learning](https://img.shields.io/badge/Focus-Explainable%20AI%20%26%20Deep%20Learning-orange)
![License](https://img.shields.io/badge/License-MIT-green)

## 📌 1. Project Context & Business Challenge
This project conducts a comprehensive analysis of **35,000+ hospital records** for hip and knee replacement surgeries over a 3-year period. As a major private health insurer (Medibank, Australia), the core challenge is to balance **Clinical Excellence** (patient recovery) with **Financial Sustainability** (cost control).

The team’s primary mission is to support three strategic initiatives:
*   **No Gap Programs:** Eliminating out-of-pocket costs for members.
*   **Best Care Initiatives:** Ensuring safety and maximizing functional outcomes (FIM scores).
*   **Short Stay Programs:** Optimizing Length of Stay (LOS) through integrated care networks.

---

## 🔍 2. Analytical Roadmap
The analysis follows a "Diagnostic -> Predictive -> Prescriptive" framework:
1.  **Diagnostic (EDA):** Identifying cost drivers, demographic trends, and operational bottlenecks.
2.  **Predictive (ML):** Building models to forecast 28-day readmission risk and total treatment costs.
3.  **Prescriptive (Optimization):** Proposing a recommender system to personalize patient pathways.

---

## 💡 3. Key Strategic Insights

### 🚀 The "Rehab Gap" Paradox (Critical Finding)
One of the most significant discoveries is the **Acute-to-Rehab Delay**. 
*   **The Myth:** Delaying rehabilitation admissions might seem like a way to save short-term rehab costs.
*   **The Reality:** Data proves a **False Economy**. While a >2 day delay reduces immediate rehab spend, it triggers a **70% surge in readmission risk** (from 5.4% to 9.2%).
*   **Financial Impact:** Saving $6,500 in rehab fees results in a potential **$25,000 loss** per readmission case. Triet-zeroing this gap is the highest priority for the **Best Care** initiative.

### 🏥 Provider Benchmarking (Best Value per Price)
Using a **Quadrant Analysis framework**, I identified "Elite Providers" (e.g., Hospital Group 27) that achieve:
*   **Ultra-low Out-of-pocket:** Average $65 vs. system average of $1,000+.
*   **High Clinical Value:** 21.0 FIM improvement with nearly 0% dependency on expensive inpatient rehab.
*   **Action:** These providers should be the backbone of the **No Gap Program** expansion.

---

## 🤖 4. Machine Learning & AI Implementation

### 📉 Risk Prediction (XGBoost + SHAP)
*   **Objective:** Predict the probability of 28-day readmission.
*   **Methodology:** XGBoost Classifier with `scale_pos_weight` to handle class imbalance.
*   **Explainability:** Used **SHAP (Explainable AI)** to "open the black box." SHAP values confirmed that `flg_complex` and `Acute_to_Rehab_Gap` are the primary risk drivers.

### 💰 Cost Forecasting (Deep Learning - ANN)
*   **Objective:** Predict total treatment cost for budget planning.
*   **Architecture:** A 4-layer Artificial Neural Network (TensorFlow/Keras) with Dropout layers for regularization.
*   **Performance:** Achieved a **Mean Absolute Error (MAE) of $3,090**, representing a **~12.3% error rate**—highly reliable for actuarial forecasting.

### 📍 Personalized Pathway (KNN Recommender)
*   **Objective:** Recommend the optimal rehab facility for new patients.
*   **Logic:** A K-Nearest Neighbors (KNN) algorithm identifies "clinical twins" from historical data to suggest providers with the highest expected FIM improvement for that specific patient profile.

---

## 📈 5. Strategic Recommendations (Actionable Insights)
1.  **Eliminate Treatment Gaps:** Digitalize the hospital-to-rehab handover to achieve "Zero-Day Delay." Every day saved is a direct contribution to the **Short Stay Program**.
2.  **Risk-Based Pricing:** Implement the developed **3D Risk Scorecard** (Age x State x Gender) to refine insurance premium models.
3.  **Preferred Provider Network:** Incentivize members to choose "Star Providers" identified in the Value-per-Price analysis to minimize Medibank's financial leakage and patient out-of-pocket spend.

---

## 🛠 6. Tech Stack
*   **Data Processing:** `Pandas`, `NumPy`
*   **Visualization:** `Seaborn`, `Matplotlib` (Custom fonts for localized reporting)
*   **Machine Learning:** `Scikit-learn`, `XGBoost`
*   **Deep Learning:** `TensorFlow`, `Keras`
*   **Model Interpretation:** `SHAP`
*   **Environment:** Google Colab / Jupyter Notebooks

---

