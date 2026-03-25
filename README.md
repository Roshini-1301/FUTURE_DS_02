# Telco Customer Churn Analysis

A comprehensive customer retention and churn analysis built on the IBM Telco Customer Churn dataset.
This project is designed to help SaaS and subscription-based businesses understand why customers leave,
identify at-risk segments, and take data-driven action to improve retention.

##  Objective

> *"Predict behavior to retain customers. Analyze all relevant customer data and develop focused customer retention programs."* — IBM Sample Data Sets

This analysis answers four core business questions:
- Why are customers leaving the platform?
- Which customer segments are most likely to churn?
- How long do customers typically stay active?
- What actions can improve customer retention?



##  Dataset

**Source:** [IBM Telco Customer Churn — Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

| Property | Detail |
|----------|--------|
| Rows | 7,043 customers |
| Columns | 21 features |
| Target variable | `Churn` (Yes / No) |

**Feature categories:**
- **Demographics** — gender, senior citizen status, partner, dependents
- **Services** — phone, internet, online security, tech support, streaming
- **Account info** — tenure, contract type, payment method, monthly & total charges



## Setup & Requirements

### Prerequisites
Make sure you have Python 3.8+ and Jupyter Notebook or JupyterLab installed.

### Install dependencies
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### Run the notebook
```bash
jupyter notebook Telco_Churn_Analysis.ipynb
```

> **Note:** Place `WA_Fn-UseC_-Telco-Customer-Churn.csv` in the same directory as the notebook before running.



## Notebook Overview

The notebook is structured across 16 sections:

| Section | Description |
|---------|-------------|
| 1–2 | Library setup, custom dark theme, data loading |
| 3 | Data cleaning — fixes blank `TotalCharges`, encodes target, creates tenure & charge bands |
| 4 | Executive summary — overall churn rate, MRR, revenue at risk |
| 5 | Churn by contract type, internet service, and payment method |
| 6 | Tenure-based churn — identifies the critical first-year window |
| 7 | Monthly charges vs churn correlation |
| 8 | Demographic segmentation — gender, senior citizen, partner, dependents |
| 9 | Add-on services protective effect analysis |
| 10 | Top churn risk factor ranking |
| 11 | Cohort heatmap — Contract Type × Tenure Band |
| 12 | Customer Lifetime Value (CLV) estimation by contract |
| 13 | Feature correlation with churn |
| 14 | High-risk vs low-risk segment profiling |
| 15 | Business insights and 5 prioritised recommendations |
| 16 | Dataset export with computed `RiskScore` per customer |



## Key Findings

- **Overall churn rate: 26.5%** — above the 15–25% industry benchmark
- **Month-to-month customers churn at 42.7%** vs only 2.8% for two-year contracts
- **Fiber optic churn: 41.9%** — 2× higher than DSL customers
- **First 12 months are the highest-risk window** — average churned customer left at 18 months
- **Online Security and Tech Support reduce churn by ~15–20 percentage points**
- **Electronic check payers churn at 45.3%** vs ~15% for auto-pay customers
- **$139,000/month** in MRR is currently at risk from churned customers



## Top Recommendations

| Priority | Action | Expected Impact |
|----------|--------|-----------------|
| High | Convert M2M customers to annual contracts | Save $18K–$22K/month |
| High | Fix Fiber optic value proposition + bundle security | Retain ~315 customers/cycle |
| Medium | Strengthen onboarding in first 90 days | Reduce overall churn by ~1.5pp |
| Medium | Migrate electronic check payers to auto-pay | Cut payment-driven churn by ~30pp |
| Low | Launch senior citizen retention program | Reduce 41.7% senior churn rate |


##  Outputs

| File | Description |
|------|-------------|
| `telco_churn_enriched.csv` | Full dataset with `RiskScore` (0–11) and `HighRisk` flag per customer |
| `churn_summary_metrics.csv` | Summary table of all key KPIs |


##  Next Steps
Train a churn prediction model (Logistic Regression / XGBoost) using the `RiskScore` features
A/B test the annual contract conversion offer on a subset of M2M customers
Build a live retention dashboard tracking churn rate, MRR at risk, and at-risk segment sizes
Conduct exit interviews with churned Fiber optic customers to validate root causes



## Tools Used

- **Python 3** — core analysis language
- **Pandas** — data manipulation and aggregation
- **NumPy** — numerical operations
- **Matplotlib** — custom visualisations with dark theme
- **Seaborn** — heatmaps and statistical plots
- **Jupyter Notebook** — interactive analysis environment

