# 📍 Suffolk County, MA — ZIP Code Desirability Analysis

An interactive Tableau dashboard analyzing ZIP code desirability across Suffolk County, MA using 2023 U.S. Census Bureau and crime data. Built to help residents, city planners, and researchers identify the most livable neighborhoods based on a composite scoring model.

---

## 🎯 Problem Statement

Choosing where to live involves balancing multiple factors — income levels, safety, education, housing costs, and population density. This project builds a **data-driven composite desirability score** for every ZIP code in Suffolk County, MA, giving users an objective, multi-dimensional view of neighborhood quality rather than relying on a single metric.

---

## 📊 Dashboard Overview

🔗 [View Live Interactive Dashboard](https://public.tableau.com/app/profile/shubham.rajiwade/viz/SuffolkCountyZIPCodeAnalysis/MainDashboard)

### Dashboard 1 — Main Dashboard
- **Score Map** — Interactive choropleth map showing composite desirability scores by ZIP code
- **Population Distribution Treemap** — Visual breakdown of population across neighborhoods
- **Score Breakdown Table** — Detailed composite, crime, housing, and education scores per ZIP
- **Top 10 ZIP Codes** — Rankings by composite desirability score

### Dashboard 2 — Detailed Variable Analysis
- Income analysis by ZIP code
- Education attainment breakdown
- Housing cost distribution
- Crime rate analysis
- KPI summary cards — Total Population, Avg Income, Avg Education, Avg Crime, Avg Housing

---

## 🧮 Scoring Methodology

Each ZIP code receives a **Composite Desirability Score (0–100)** based on five weighted variables:

**Composite Score = (Income × 25%) + (Education × 20%) + (Housing × 20%) + (Crime × 20%) + (Population × 15%)**

| Variable | Weight | Rationale |
|---|---|---|
| Median Household Income | 25% | Strongest correlator with quality of life and access to services |
| Education Level | 20% | Reflects community workforce quality and attainment |
| Housing Cost | 20% | Indicates market desirability and property values |
| Crime Rate | 20% | Critical safety indicator — inverse scored (lower crime = higher score) |
| Population | 15% | Mixed implications — amenities vs. congestion |

**Data Normalization:** All variables normalized to 0–100 scale using min-max normalization for fair contribution across metrics.

---

## 📈 Key Findings

| Metric | Suffolk County Value |
|---|---|
| Total Population | 777,732 |
| Average Household Income | $99,871 |
| Average Education (Bachelor's+) | 60.74% |
| Average Crime Rate | 25.98 per 1,000 |
| Average Housing Value | $740,200 |

**Top ZIP Codes by Composite Score:**
| ZIP | City | Composite Score |
|---|---|---|
| 02108 | Boston | 78.5% |
| 02210 | Boston | 75.3% |
| 02116 | Boston | 69.2% |
| 02109 | Boston | 65.9% |
| 02129 | Charlestown | 62.5% |

---

## 🗂️ Data Sources

- U.S. Census Bureau — American Community Survey 5-Year Estimates (2019–2023): Demographics, Housing, Income, Education via [data.census.gov](https://data.census.gov)
- NeighborhoodScout — Crime rates based on FBI Uniform Crime Report data (2023)

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Tableau Public | Interactive dashboard design and visualization |
| Microsoft Excel | Data preparation, normalization, composite score calculation |
| U.S. Census Bureau API | Demographic and economic data sourcing |
| GitHub | Version control and documentation |

---

## 📂 Repository Structure

```
suffolk-county-zip-analysis/
│
├── README.md
├── data/
│   ├── suffolk_zipcode_data.xlsx        # Cleaned dataset with composite scores
│   └── methodology_document.docx        # Full scoring methodology
├── tableau/
│   └── suffolk_county_zip_analysis.twb  # Tableau workbook
├── eda/
│   └── suffolk_eda.ipynb               # Exploratory Data Analysis notebook
└── screenshots/
    ├── main_dashboard.png
    └── detailed_analysis.png
```

---

## 🔍 Analytical Approach

- **Data Collection** — Gathered demographic, economic, housing, and crime data from Census Bureau and NeighborhoodScout
- **Normalization** — Applied min-max normalization to standardize all variables to 0–100 scale
- **Composite Scoring** — Built weighted scoring model balancing five quality-of-life indicators
- **Visualization** — Designed interactive Tableau dashboards with map, treemap, rankings, and KPI views
- **Insight Generation** — Identified top and bottom performing ZIP codes with actionable insights

---

## 💡 Potential Applications

- **Real Estate** — Help buyers identify high-value neighborhoods
- **City Planning** — Identify underserved areas needing investment
- **Public Policy** — Target resources to low-scoring ZIP codes
- **Research** — Academic analysis of urban neighborhood quality

---

## 📝 License
This project is licensed under the MIT License.
