# Working Hard, Earning Less?  
**A data analysis of hospitality wages in Ireland**  

**Author:** <Clarissa>  
**Date:** <YYYY-MM-DD>  

## Short description
This project analyses earnings in the hospitality sector (Accommodation & Food Service Activities) in Ireland using official CSO statistics. It compares average weekly and hourly earnings and hours worked against the national average to understand the wage gap and how wages have evolved (2008–2025).

## Motivation
I worked in hospitality for several years and wanted to use public data to explore whether wages in the sector have kept pace with broader labour market trends and inflation. This project is intended for my portfolio to demonstrate data cleaning, EDA and storytelling with real government data.

## Data sources
- **CSO – EHQ03 / EHQ12 / EHA04** (selected statistics): Average Weekly Earnings, Average Hourly Earnings, Average Weekly Paid Hours (Quarterly / Annual).  
  *Access via CSO StatBank – search table `EHQ03` (Average Earnings, Hours Worked, Employment and Labour Costs).*
- **CSO – CPI** (for inflation adjustment) — table `CPM12` or equivalent.

**Filters used for analysis**
- Metrics: `Average Weekly Earnings (Euro)`, `Average Hourly Earnings (Euro)`, `Average Weekly Paid Hours (Hours)`
- Sectors: `Accommodation and food service activities (I)` and `All NACE economic sectors`
- Period: 2008Q1 – 2025Q1 (quarterly) / 2008 – 2024 (annual where applicable)

## Project structure
hospitality_wages_project/
├── data/
│ ├── raw/ # original downloads (CSV)
│ └── processed/ # cleaned CSVs used in notebooks
├── notebooks/
│ ├── 01_data_cleaning.ipynb
│ ├── 02_eda.ipynb
│ └── 03_analysis.ipynb
├── outputs/
│ ├── charts/
│ └── tables/
└── README.md

# Project roadmap

| Step | Purpose | Notebook / File | Core actions | Time (est.) |
|---|---:|---|---|---:|
| 1. Data download | Get raw CSO exports (EHQ03 / EHA04 / CPI) | `data/raw/` | Download CSV(s) from CSO StatBank; save with `YYYY-MM-DD_*.csv` | 1–2h |
| 2. Clean & organize | Make tidy dataset for analysis | `notebooks/01_data_cleaning.ipynb` / `data/processed/` | Columns, types, quarter → Period, sector names, filter metrics | 2–3h |
| 3. EDA (exploratory) | Understand patterns & data quality | `notebooks/02_eda.ipynb` | Summary stats, missing values, visual checks (time series, hours vs pay) | 2–4h |
| 4. Analysis & visuals | Build final plots & comparisons | `notebooks/03_analysis.ipynb` / `outputs/charts/` | Line charts, gap/ratio plots, bar charts, % change tables | 3–5h |
| 5. Storytelling & write-up | Add narrative & personal insight | `README.md`, notebook markdown | Interpret results, link to policy/events, personal reflection | 1–2h |
| 6. Publish | Share on GitHub / optional Streamlit | `.` | Push repo, add screenshots, optionally deploy app | 1–2h |

## Notebooks produced: 

01_data_cleaning.ipynb → produces processed CSV in data/processed/

02_eda.ipynb → exploratory charts and tables

03_analysis.ipynb → final visuals and narrative
