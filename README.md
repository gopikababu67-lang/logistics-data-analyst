# logistics-data-analyst
Logistics analytics project — data cleaning, EDA &amp; Random Forest predictive modeling (R²=0.71) to forecast delivery delays for a simulated logistics

# 🚚 SwiftCargo Logistics Analytics — Delivery Performance & Delay Prediction

[![Python](https://img.shields.io/badge/Python-3.10-blue.svg)]()
[![Status](https://img.shields.io/badge/Status-Complete-brightgreen.svg)]()
[![License](https://img.shields.io/badge/License-MIT-lightgrey.svg)]()

Complete 4 tasks data analytics project completed during the **Logistics Data Analyst Intern** internship on Yuva Intern (NSDC).
The project analyzes delivery performance for a simulated last-mile logistics company, **SwiftCargo Logistics Pvt. Ltd.**, culminating in a predictive model for delivery delays and data-driven optimization recommendations.

GitHub: [@gopikababu67]

· LinkedIn: www.linkedin.com/in/gopikababu17

## Author
**Gopika** — B.Tech AI & Data Science, Prathyusha Engineering College (Autonomous), Chennai

## Problem Statement
SwiftCargo Logistics operates across 5 Indian cities (Chennai, Bengaluru, Hyderabad, Mumbai, Delhi) with a mixed fleet of bikes, vans, mini trucks and heavy trucks. Out of 2,000 recent shipments, only **52.2% were delivered on time**. This project identifies the drivers of delay and builds a predictive model to forecast and reduce it.

## 🎯 Objectives
- Define measurable KPIs to quantify delivery and cost performance
- Build a clean, analysis-ready dataset through a documented preprocessing pipeline
- Identify the key drivers of delivery delay through exploratory analysis
- Develop a predictive model to forecast delivery time and delay risk
- Translate findings into concrete, prioritized operational recommendations

## Key Performance Indicators (KPIs)
| KPI | Value |
|---|---|
| On-Time Delivery Rate | 52.20% |
| Average Delivery Time | 4.19 days |
| Average Cost per Shipment | ₹3083.86 |
| Delay Severity | 2.51 days |

## Tech Stack
- Python 3 (Google Colab)
- Pandas, NumPy — data handling
- Matplotlib, Seaborn — visualization
- Scikit-learn — predictive modelling (Random Forest, Linear Regression)

## Project Structure

├── logistics-data-analyst-internship.ipynb → Full Colab notebook (all 4 weeks)
├── Task1_Strategic_Planning_Logistics_Gopika.docx
├── Task2_Data_Cleaning_Preprocessing_Gopika.docx
├── Task3_EDA_Visualization_Logistics_Gopika.docx
├── Task4_Predictive_Modeling_Optimization_Gopika.docx
├── swiftcargo_logistics.csv → Original simulated dataset (2000 rows, 13 cols)
├── swiftcargo_logistics_RAW.csv → Deliberately "dirtied" raw dataset (2015 rows)
├── swiftcargo_logistics_CLEANED.csv → Cleaned, analysis-ready dataset (2000 rows, 16 cols)
├── chart1_delivery_distribution.png
├── chart2_weather_delay.png
├── chart3_correlation_heatmap.png
├── chart4_cost_by_vehicle.png
├── chart5_distance_vs_time.png
├── chart6_ontime_by_city.png
└── README.md


## Task 1 — Strategic Planning
Defined the SwiftCargo scenario, 5 KPIs, researched public logistics datasets and applicable data science techniques (regression, classification, clustering, optimization), and built an end-to-end analysis roadmap. Generated a reproducible 2,000-shipment dataset.

📄 `Week1_Strategic_Planning_Logistics_Gopika.docx`

## Task 2 — Data Collection, Cleaning & Preprocessing
Simulated a realistic "dirty" raw dataset (81 missing values × 4 columns, 15 duplicates, outliers, inconsistent text). Built a full preprocessing pipeline: duplicate removal, text standardization, median/mode imputation, IQR-based outlier capping, and Min-Max normalization. Result: 2,000 clean rows, 0 missing values.

📄 `Week2_Data_Cleaning_Preprocessing_Gopika.docx`

## Task 3 — Exploratory Data Analysis & Visualization
Computed descriptive statistics and a correlation matrix, revealing Distance_KM is the strongest driver of delivery time (r = 0.77) while Promised_Days is statistically unrelated to actual delivery (r = 0.01). Produced 6 visualizations analyzing delivery time distribution, weather impact, cost by vehicle type, and city-level performance.

📄 `Week3_EDA_Visualization_Logistics_Gopika.docx`

## Task 4 — Predictive Modeling & Optimization
Built a Random Forest regression model (R² = 0.709, MAE = 0.649 days, 5-fold CV mean R² = 0.733) to forecast delivery duration, and a Random Forest classifier (62% accuracy, 60% recall) to predict delay risk. Translated results into 4 optimization strategies: data-driven promise recalibration, weather-aware buffering, risk-based shipment triage, and continuous data enrichment.

📄 `Week4_Predictive_Modeling_Optimization_Gopika.docx`

## Key Findings
- **Distance is the #1 delay driver** — 68.9% feature importance in the predictive model
- **Delivery promises are disconnected from reality** — near-zero correlation with actual delivery time
- **Storms cause severe delays** — only ~21% on-time rate during storm conditions
- **Vehicle type does not significantly affect fuel cost** — cost optimization should focus on route planning, not fleet substitution

## 🔍 Methodology
1. **Data Simulation** — Generated a realistic shipment dataset with controlled randomness (fixed seed) for reproducibility
2. **Data Cleaning** — Applied industry-standard techniques (IQR outlier capping, median/mode imputation) chosen specifically to avoid distorting the dataset
3. **EDA** — Used correlation analysis and 6 purpose-selected visualizations to identify delay drivers before modeling
4. **Modeling** — Compared a Linear Regression baseline against Random Forest; validated with 5-fold cross-validation to confirm generalization
5. **Optimization** — Mapped every model insight to a specific, actionable business recommendation

---

## 📈 Results Summary

| Model | Metric | Score |
|---|---|---|
| Random Forest Regressor | R² | 0.709 |
| Random Forest Regressor | MAE | 0.649 days |
| Random Forest Regressor | 5-Fold CV Mean R² | 0.733 |
| Random Forest Classifier | Accuracy | 62.0% |
| Random Forest Classifier | Recall (Delayed) | 60.0% |

**Top predictive features:** Distance_KM (68.9%) → Weather_Clear (11.2%) → Weight_KG (8.0%)

---

## 💡 Key Findings
- **Distance is the #1 delay driver** — accounts for 68.9% of the predictive model's decision-making
- **Delivery promises are disconnected from reality** — near-zero correlation (r = 0.01) with actual delivery time, meaning promises are set by convention, not data
- **Storms severely affect reliability** — only ~21% on-time rate during storm conditions vs ~58% in clear weather
- **Vehicle type barely affects fuel cost** — cost optimization should focus on route planning and load consolidation, not fleet substitution

## 🚀 Optimization Recommendations
1. **Recalibrate delivery promises** using model-predicted delivery time instead of fixed convention
2. **Weather-aware dispatch buffering** — add proactive time buffers when storms/rain are forecast
3. **Risk-based shipment triage** — flag high-risk shipments using the classifier for priority handling
4. **Continuous data enrichment** — capture traffic and warehouse dispatch data to improve future model accuracy

---

## ▶️ How to Run This Project
1. Open `logistics-data-analyst-internship.ipynb` in [Google Colab](https://colab.research.google.com)
2. Run all cells in order (Runtime → Run all)
3. This regenerates the dataset, cleaning pipeline, visualizations and models from scratch
4. Outputs (CSVs, charts) will be saved in the Colab session and can be downloaded

---

## 🔮 Future Work
- Incorporate real-time traffic and weather API data
- Deploy the model as a simple web app for live delay-risk scoring
- Expand to route optimization using linear programming
- Test additional models (XGBoost, Gradient Boosting) for potential accuracy gains


## Status
- ✅ Week 1 — Strategic Planning
- ✅ Week 2 — Data Cleaning & Preprocessing
- ✅ Week 3 — EDA & Visualization
- ✅ Week 4 — Predictive Modeling & Optimization

**Project Complete ✅**
