# Employee Attrition Analytics Dashboard — Tableau Project

**Type:** Independent Portfolio Project
**Timeline:** December 2025 – January 2026
**Tools:** Tableau Public
**Dataset:** [IBM HR Analytics Employee Attrition](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset) — 1,470 rows, 35 fields
**Live Dashboard:** *(Add your Tableau Public link here after publishing)*

---

## Project Overview

Built an interactive 3-view Tableau Public dashboard analyzing employee attrition patterns across an IBM HR dataset. The dashboard allows HR stakeholders to explore attrition by department, tenure, and compensation — all linked via a single Department filter — and surfaces the highest-risk employee cohort for targeted retention action.

---

## Dashboard Views

### View 1 — Attrition by Department (Bar Chart)
Compares attrition rate and count across Sales, R&D, and Human Resources departments.

### View 2 — Attrition by Tenure Band (Heatmap)

| Tenure Band | Attrition Rate |
|---|---|
| 0-1 year | ~31% (highest) |
| 1-3 years | ~24% |
| 3-5 years | ~14% |
| 5+ years | ~8% |

### View 3 — Monthly Income vs. Attrition Rate (Scatter Plot)
- X-axis: Monthly income bucket ($1k-$2k, $2k-$3k, $3k-$5k, $5k+)
- Y-axis: Attrition rate %
- Colored by job role

---

## Key Finding

> **Sales Representatives under 2 years of tenure earning below $3,000/month showed a 52% attrition rate** — the highest-risk cohort in the dataset.

This cohort was annotated directly on the dashboard for non-technical HR stakeholders.

---

## How to Reproduce

1. Download `WA_Fn-UseC_-HR-Employee-Attrition.csv` from [Kaggle](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
2. Open [Tableau Public](https://public.tableau.com/) (free)
3. Connect to the CSV file
4. Build the 3 views described above
5. Link all sheets with a Department filter
6. Annotate the 52% attrition finding on the scatter plot
7. Publish to Tableau Public and paste your link above

---

## Repository Structure

```
employee-attrition-tableau/
├── docs/
│   ├── executive_summary.md      # Plain-language findings report
│   └── dashboard_build_guide.md  # Step-by-step Tableau instructions
└── README.md
```

---

## Skills Demonstrated

- Tableau Public multi-view dashboard design
- KPI definition and cohort analysis
- Data storytelling for non-technical stakeholders
- Executive summary writing
- HR analytics domain knowledge
