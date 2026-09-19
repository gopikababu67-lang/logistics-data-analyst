# logistics-data-analyst
Logistics analytics project — data cleaning, EDA &amp; Random Forest predictive modeling (R²=0.71) to forecast delivery delays for a simulated logistics

# Logistics Data Analyst Internship — SwiftCargo Logistics Analysis

Complete 4 tasks data analytics project completed during the **Logistics Data Analyst Intern** internship on Yuva Intern (NSDC).
The project analyzes delivery performance for a simulated last-mile logistics company, **SwiftCargo Logistics Pvt. Ltd.**, culminating in a predictive model for delivery delays and data-driven optimization recommendations.

## Author
**Gopika** — B.Tech AI & Data Science, Prathyusha Engineering College (Autonomous), Chennai

## Problem Statement
SwiftCargo Logistics operates across 5 Indian cities (Chennai, Bengaluru, Hyderabad, Mumbai, Delhi) with a mixed fleet of bikes, vans, mini trucks and heavy trucks. Out of 2,000 recent shipments, only **52.2% were delivered on time**. This project identifies the drivers of delay and builds a predictive model to forecast and reduce it.

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
├── Week1_Strategic_Planning_Logistics_Gopika.docx
├── Week2_Data_Cleaning_Preprocessing_Gopika.docx
├── Week3_EDA_Visualization_Logistics_Gopika.docx
├── Week4_Predictive_Modeling_Optimization_Gopika.docx
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


## Week 1 — Strategic Planning
Defined the SwiftCargo scenario, 5 KPIs, researched public logistics datasets and applicable data science techniques (regression, classification, clustering, optimization), and built an end-to-end analysis roadmap. Generated a reproducible 2,000-shipment dataset.

📄 `Week1_Strategic_Planning_Logistics_Gopika.docx`

## Week 2 — Data Collection, Cleaning & Preprocessing
Simulated a realistic "dirty" raw dataset (81 missing values × 4 columns, 15 duplicates, outliers, inconsistent text). Built a full preprocessing pipeline: duplicate removal, text standardization, median/mode imputation, IQR-based outlier capping, and Min-Max normalization. Result: 2,000 clean rows, 0 missing values.

📄 `Week2_Data_Cleaning_Preprocessing_Gopika.docx`

## Week 3 — Exploratory Data Analysis & Visualization
Computed descriptive statistics and a correlation matrix, revealing Distance_KM is the strongest driver of delivery time (r = 0.77) while Promised_Days is statistically unrelated to actual delivery (r = 0.01). Produced 6 visualizations analyzing delivery time distribution, weather impact, cost by vehicle type, and city-level performance.

📄 `Week3_EDA_Visualization_Logistics_Gopika.docx`

## Week 4 — Predictive Modeling & Optimization
Built a Random Forest regression model (R² = 0.709, MAE = 0.649 days, 5-fold CV mean R² = 0.733) to forecast delivery duration, and a Random Forest classifier (62% accuracy, 60% recall) to predict delay risk. Translated results into 4 optimization strategies: data-driven promise recalibration, weather-aware buffering, risk-based shipment triage, and continuous data enrichment.

📄 `Week4_Predictive_Modeling_Optimization_Gopika.docx`

## Key Findings
- **Distance is the #1 delay driver** — 68.9% feature importance in the predictive model
- **Delivery promises are disconnected from reality** — near-zero correlation with actual delivery time
- **Storms cause severe delays** — only ~21% on-time rate during storm conditions
- **Vehicle type does not significantly affect fuel cost** — cost optimization should focus on route planning, not fleet substitution

## Status
- [x] Week 1 — Strategic Planning
- [x] Week 2 — Data Cleaning & Preprocessing
- [x] Week 3 — EDA & Visualization
- [x] Week 4 — Predictive Modeling & Optimization

**Project Complete ✅**
