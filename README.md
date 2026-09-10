# PMO Project Performance Intelligence

> **Portfolio Demonstration Project using synthetic PMO data.** No Southern Nuclear, Southern Company, JP Morgan, or CVS Health confidential data is used or represented anywhere in this repository. All datasets are synthetically generated for the sole purpose of demonstrating analytical approach, technical execution, and reporting design.

## Business Problem

A Project Management Office receives project information from multiple, disconnected sources: a project management system, weekly status updates submitted by project managers, financial/cost reporting, schedule tracking, milestone logs, risk registers, and issue trackers. These sources disagree with each other, contain missing or invalid values, and are not always current.

**Central business question:**
*How can a PMO consolidate fragmented project information, validate the data, identify performance trends and risks, and provide leadership with a clear, actionable view of portfolio health?*

This repository answers that question end-to-end: from raw, messy multi-source data through validation, integration, SQL/Python analysis, KPI governance, and executive reporting design.

## The Data Story

```
MESSY MULTI-SOURCE DATA
        |
DATA QUALITY VALIDATION
        |
DATA CLEANING
        |
DATA INTEGRATION (star schema)
        |
SQL ANALYSIS (12 scripts)
        |
KPI GOVERNANCE (RAG logic)
        |
PROJECT PERFORMANCE (schedule / cost / risk)
        |
POWER BI EXECUTIVE REPORTING (design)
        |
EXECUTIVE INSIGHTS
        |
LEADERSHIP DECISION SUPPORT
```

## Repository Structure

```
data/                 12 synthetic source datasets (intentionally messy)
sql/                  12 SQL analysis scripts, each answering a business question
python/               Data cleaning, validation, ETL, KPI, EDA, forecasting scripts
docs/
  data-model.md       Star schema, fact/dimension tables, grain, relationships
  data-quality.md     Data quality framework, rules, and computed results
  reconciliation.md   Multi-source status reconciliation logic
  kpi-governance.md   KPI dictionary: definition, formula, threshold, RAG, action
  rag-logic.md        Project health scoring logic (Green/Amber/Red)
  powerbi-design.md   8-page executive dashboard design + DAX measures
  screen-share-guide.md  Interview walkthrough script
reports/
  executive-insights.md  Observation -> Driver -> Impact -> Recommendation
docs/pages/           GitHub Pages interactive experience (static site)
```

## Key Findings (Computed From This Repository's Data)

Running `sql/12_executive_summary.sql` and `python/kpi_analysis.py` against the 42-project synthetic portfolio produces:

- **21 Green / 19 Amber / 7 Red** projects by computed project health
- **17 of 42 projects (40%)** show forecast cost variance greater than 15%
- **19 open risks**, of which **11 are High or Critical**
- **23 open issues** across the portfolio
- **Overall data quality score: 95.3%**, with 31 rule failures identified across 655 records in 13 documented categories (missing IDs, duplicate records, invalid ratings, orphan records, stale updates, etc.)

These numbers are the actual output of the scripts in this repo, not illustrative placeholders — see `reports/executive-insights.md` for the full interpretation.

## Positioning

This project demonstrates capability as a **Business Intelligence & Project Performance Analyst**: multi-source data validation, SQL and Python analytics, KPI governance design, RAG reporting logic, and executive dashboard design for PMO / project-controls audiences. It is not a data-science or machine-learning portfolio piece.

## What This Is Not

- Not a claim of Southern Nuclear, Southern Company, JP Morgan, or CVS Health project data or systems.
- Not a working `.pbix` file (Power BI Desktop binary files cannot be authored through this toolchain) — the Power BI section is a documented design (pages, measures, DAX) intended to be built out in Power BI Desktop.
- Not a predictive model claiming production-grade accuracy — the forecasting script documents its method, assumptions, and limitations transparently.
