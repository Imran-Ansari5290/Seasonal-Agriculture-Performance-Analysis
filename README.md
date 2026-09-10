# Seasonal Agriculture Performance Analysis

A data analytics project examining how farming practices, environmental conditions, resource usage
and economic outcomes vary across the **Kharif, Rabi and Zaid** growing seasons in India.

---

## Overview

Agricultural performance is shaped by seasonal shifts in weather, resource availability and market
conditions — but raw farm-level data rarely makes those patterns obvious on its own. This project
analyzes **4,000 farm records** across 3 seasons, 8 crops, 8 states and 4 irrigation methods to
uncover the seasonal patterns, relationships and differences that actually drive yield and profit.

The full workflow — cleaning, exploratory analysis, correlation analysis, seasonal comparison, and
three original designed analyses — is documented end-to-end in a single notebook.

## Objectives

- Explore, clean and prepare the raw agricultural dataset
- Examine how performance varies across seasons
- Identify relationships between environmental conditions and outcomes
- Compare economic performance (cost, revenue, profit) across seasons, crops, states and irrigation methods
- Surface unusual/unexpected patterns and turn them into evidence-based recommendations

## Dataset

| | |
|---|---|
| **File** | `seasonal_agriculture_performance_dataset.csv` |
| **Records** | 4,000 farms |
| **Columns** | 28 |
| **Seasons** | Kharif, Rabi, Zaid |
| **Crops** | Rice, Wheat, Maize, Cotton, Sugarcane, Pulses, Groundnut, Chilli |
| **States** | 8 (incl. Punjab, Maharashtra, Andhra Pradesh, Karnataka …) |
| **Irrigation methods** | Drip, Sprinkler, Flood, Rainfed |

**Feature groups:**
- **Farming practices** — Crop, Season, Irrigation Method, Farm Area Hectares
- **Environmental conditions** — Rainfall_mm, Avg_Temperature_C, Humidity_pct, Sunlight_Hours_Day, Soil_pH, Soil_Moisture_pct
- **Resource usage** — Nitrogen/Phosphorus/Potassium_kg_ha, Fertilizer_kg_ha, Pesticide_Litre_ha, Water_Used_m3, Seed_Quality_Score
- **Production** — Yield_Tonnes_Ha, Production_Tonnes, Water_Efficiency_t_per_1000m3, Disease_Pest_Risk_pct
- **Economics** — Market_Price_INR_Tonne, Total_Cost_INR, Revenue_INR, Profit_INR

## Technology Used

| Purpose | Library |
|---|---|
| Data handling | `pandas`, `numpy` |
| Visualization | `matplotlib`, `seaborn` |
| Environment | Jupyter Notebook (Kaggle) |

## Project Structure

```

├── Seasonal_Agriculture_Performance_Analysis.ipynb
├── Figures
├── dataset
│   └── seasonal_agriculture_performance_dataset.csv
├── Major_Project_Seasonal_Agriculture_Performance_Analysis.pdf
└── README.md
```

## Notebook Walkthrough

| # | Section |
|---|---|
| 1–2 | Introduction, Problem Statement, objective, Import Libraries |
| 3–5 | Load dataset · first look · shape / dtypes |
| 6–8 | Missing value analysis · cleaning (season-wise median imputation) · duplicate check |
| 9–10 | Descriptive statistics · outlier detection (IQR method) |
| 11–14 | Univariate → bivariate → multivariate → correlation analysis |
| 15 | Highest and Lowest Yield and Profit Records |
| 16 | Seasonal comparison (yield, profit, water use, loss rate) |
| 17–19 | **Designed analyses:** irrigation efficiency vs. profit · state-wise profit consistency · crop profitability & loss rates |
| 20–22 | Key insights · limitations · conclusion |

## Key Findings

- **≈49% of all farms operate at a loss** — the single biggest finding, cutting across crops and seasons.
- **Zaid is the weakest season economically** (≈64% loss rate) versus Kharif (≈42%), despite Zaid also seeing the least rainfall.
- **Crop choice drives profitability far more than weather does.** Sugarcane and Chilli are strongly profitable; Wheat, Rice, Maize and Pulses average at or below break-even.
- **Water efficiency (r ≈ 0.91), not rainfall (r ≈ 0.03), is the strongest driver of yield** — irrigation management matters more than natural rainfall.
- **Drip irrigation delivers the best profit-to-water ratio**, while Flood irrigation is both the least efficient and among the least profitable.
- **State performance is uneven:** Punjab and Maharashtra lead on average profit; Andhra Pradesh has the lowest average profit and highest volatility.

*(Full list of 12 documented insights is in Section 19 of the notebook.)*

## How to Run

1. Open the notebook on **Kaggle** (or upload it to a new Kaggle Notebook).
2. Attach the dataset: `imranansariiii/seasonal-agriculture-performance-dataset`
   *(the notebook expects it at `/kaggle/input/datasets/imranansariiii/seasonal-agriculture-performance-dataset/seasonal_agriculture_performance_dataset.csv`)*
3. Run All cells — no additional setup required; all libraries used are pre-installed on Kaggle.

## Recommendations

- Prioritize efficient irrigation (Drip/Rainfed) over Flood irrigation to raise yield without increasing water use.
- Re-evaluate crop and resource support for the Zaid season, given its high loss rate.
- Encourage diversification toward higher-value crops where agro-climatically viable.
- Direct targeted support (insurance, price stabilization) toward high-volatility states like Andhra Pradesh.

## Limitations

- Cross-sectional dataset — no multi-year, farm-level trend tracking.
- Correlation findings do not establish causation.
- Limited to 8 states, 8 crops, 4 irrigation methods and 3 seasons; findings may not generalize beyond this scope.

## License

This Data Analytics project is for academic purposes.
