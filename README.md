# Telco Customer Churn Prediction & Decision Modeling

## 📌 Project Overview
End-to-end churn analysis for a telecom provider: cleaned and analyzed **7,043 
customer records**, trained a Random Forest classifier to predict churn, and 
**optimized the decision threshold to maximize retention campaign ROI** — 
because catching at-risk customers matters more than raw accuracy.

## 🎯 Business Problem
A telecom company loses ~25% of customers annually, and acquiring new customers 
costs **5x more** than retaining existing ones. Goal: predict likely churners, 
identify root causes, and set the optimal cutoff for retention calls.

## 🔍 Key Findings (EDA)
| Driver | Insight |
|---|---|
| **Contract type** | Month-to-month: **42.71% churn** · One-year: 11.27% · Two-year: **2.83%** |
| **Tenure** | 0–1 yr: **47.68% churn** · 4+ yrs: only **9.51%** — new customers are the riskiest |
| **Churn base rate** | 26.5% of all customers |

**Root causes:** contract flexibility and early tenure dominate churn risk.

## ⚙️ Approach
1. **Data Cleaning** — converted `TotalCharges` (string → float), imputed missing values with median, encoded target
2. **EDA** — churn rates by contract type, tenure buckets, charges
3. **Preprocessing** — one-hot encoding (30 features), StandardScaler on numeric features
4. **Modeling** — Random Forest Classifier (80/20 stratified split)
5. **Decision Threshold Modeling** — Precision-Recall trade-off analysis, F1-optimal threshold

## 📊 Results
| Metric | Default Threshold | Optimized (0.28) |
|---|---|---|
| Accuracy | **78.78%** | 74% |
| **Churn Recall** | 50% | **77%** ⭐ |
| Churn Precision | 63% | 51% |

**Business impact:** At the optimal threshold (0.28), recall jumped from 50% → **77%** — 
**287 of 374** actual churners identified (vs only 186 before). For retention campaigns, 
missing a churner is costlier than a false alarm — so this trade-off directly improves ROI.

## 📂 Repository Contents
| File | Description |
|---|---|
| `telco_churn_analysis.ipynb` | Full analysis notebook (5 tasks, code + outputs + charts) |

## 🛠️ Tools & Technologies
Python · Pandas · scikit-learn · Matplotlib · GitHub

## 👤 Author
**Mehak Jilani** — Data Analyst (Volunteer), CadetX UK Work Experience

[🔗 LinkedIn Profile](https://www.linkedin.com/in/mehak-jilani)

