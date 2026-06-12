# 2016 to 2025 Labor Market: OECD Analysis

**By Luiza Lopes · June 2026**

Analyzed OECD employment data (2016-2025) across 38 countries using Python and Tableau. Built a multi-dashboard report covering gender employment gaps, age group composition, and pandemic recovery trajectories. Data preprocessing included SDMX metadata parsing, data quality flagging, and multi-source relationship modeling in Tableau using FIXED LOD expressions and diverging color encoding. Key findings: the gender gap narrowed from 10.7pp to 8.7pp; older workers gained workforce share; youth employment took the hardest pandemic hit but recovered fastest.

---

## Key Findings

- **Gender gap narrowed** from 10.7pp (2016) to 8.7pp (2024), driven by female employment gains — not male decline
- **COVID-19 shock** caused the sharpest single-quarter drop in the dataset (45,414K jobs, Q1→Q2 2020); OECD aggregate recovered to pre-pandemic levels by Q1 2022
- **Older workers (55–64)** gained +1.8pp of workforce share over the decade — the most consequential structural shift in the dataset
- **Youth employment** was the most volatile group, taking the steepest 2020 hit but rebounding fastest by 2021

---

## Dashboards

Built in Tableau Public · 7 dashboards · 12+ charts

| Section | Dashboards |
|---|---|
| Overview | Employment rate map · COVID-19 recovery heatmap |
| Gender Analysis | Average rates by sex · Gender gap narrowing 2016–2024 |
| Age Analysis | Workforce composition by age group · YoY change & share shift |
| Data Quality | Estimation flags · 2025 population coverage |

🔗 [View on Tableau Public](#) *(https://public.tableau.com/views/2016to2025LaborMarketOECDAnalysis/Overview1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)*

---

## Repository Structure
oecd-labor-market-analysis/
│
├── README.md
├── .gitignore
│
├── data/
│   ├── raw/                  # original OECD downloads (not versioned)
│   │   └── .gitkeep
│   └── processed/            # preprocessed CSVs (output of notebook)
│
└── notebooks/
    └── project_2_data_prep_v2.ipynb


---

## Data Sources

All datasets downloaded directly from the [OECD Data Explorer](https://data-explorer.oecd.org):

| Dataset | Description |
|---|---|
| [Employed population — Quarterly](https://data-explorer.oecd.org/vis?df[id]=DSD_LFS%40DF_IALFS_EMP_Q&df[ag]=OECD.SDD.TPS&df[vs]=1.0&dq=...Q&pd=2016-Q1%2C2025-Q4) | Employment by age group & sex, quarterly, 38 OECD countries |
| [Employed population — Annual](https://data-explorer.oecd.org/vis?df[id]=DSD_LFS%40DF_IALFS_EMP_Q&df[ag]=OECD.SDD.TPS&df[vs]=1.0&dq=...A&pd=2016%2C2025) | Employment by age group & sex, annual, 38 OECD countries |
| [Historical population (POPHIST)](https://data-explorer.oecd.org/vis?df[id]=DSD_POPULATION%40DF_POP_HIST&df[ag]=OECD.ELS.SAE&df[vs]=1.0) | Working-age population by sex, used as employment rate denominator |

---

## How to Run

1. Clone the repository
2. Download the raw CSVs from the links above and place them in `data/raw/`
3. Run `notebooks/project_2_data_prep_v2.ipynb` — preprocessed files will be saved to `data/processed/`
4. Open the Tableau workbook and relink the data sources to `data/processed/` if needed

**Requirements:** Python 3.x · pandas

---

## Tools & Skills

`Python` `pandas` `Tableau Public` `Dashboard Design`
