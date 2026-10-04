# Credit Loan Portfolio Vintage & RCA Dashboard

Maps to: Credit Risk intern role — portfolio monitoring, RCAs, patterns in data.

## Dataset
Lending Club loan data (Kaggle, 2007–2018) — ~2.2M loans with grades, DPD/charge-off status, FICO, DTI, income, purpose.

## Scope
- Clean and load data into SQLite/PostgreSQL.
- SQL for **vintage curves** (cumulative default rate by origination quarter vs. months on book), **roll rates** (current → 30 → 60 → 90+ DPD), and **delinquency by segment**.
- Run an **RCA** on a worsening vintage (e.g. 2015–2016 cohorts) and decompose the deterioration by grade, DTI band, purpose, term, and income bracket.
- Build a **Tableau dashboard**: portfolio KPIs, vintage curves, drill-downs by segment.
- Short **policy recommendation memo**: e.g. "tightening DTI cutoff above X in grade D–E would reduce expected loss by Y% at Z% approval cost."

## Structure
```
data/raw/              # Lending Club CSV (gitignored, large)
data/derived/          # cleaned SQLite/Parquet files
sql/                   # vintage_curves.sql, roll_rates.sql, delinquency_by_segment.sql, rca_worsening_vintage.sql
notebooks/             # 01_eda.ipynb, 03_rca_worsening_vintage.ipynb
tableau/               # portfolio_health_dashboard.twbx
docs/policy_memo.md    # the lending-memo-friendly writeup
README.md              # this file
```

## Status
Scaffold only — content coming overnight. See commits for progress.

## Resume bullet
> Credit Portfolio Monitoring and RCA Dashboard | GitHub, Tableau | 2025
> Built SQL/Tableau pipeline on 2M+ Lending Club loans for vintage curves, roll-rate matrices and segment delinquency; ran RCA on deteriorating cohorts and proposed DTI/grade cut-off changes with quantified loss-vs-approval trade-off.