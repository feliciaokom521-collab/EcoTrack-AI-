# EcoTrack AI 
### Environmental Waste Hotspot Analysis — Urban Nigerian Communities

> *Predicting where Nigeria's urban waste management system is failing, why it is failing, and what to do about it.*

---

## The Problem

Urban waste mismanagement in Nigeria is a compounding crisis. Illegal dumping blocks drainage channels. Blocked drainage causes flooding. Flooding spreads waste further and blocks more drainage. Decision-makers lack a data-driven way to identify which communities need intervention first — and which interventions will actually work.

EcoTrack AI addresses that gap.

---

## What This Project Does

This project analyses **1,000 urban communities across 12 Nigerian states** using a weighted risk scoring model built on four environmental indicators. It identifies which communities are in crisis, which are heading there, and where targeted investment will produce the greatest impact.

**Tools used:** Python · Microsoft Excel · Power BI · DAX

---

## Key Findings

**🔴 149 communities are in Critical condition** — and 33% of them are in a single state (Borno), despite Borno representing only 7.6% of all communities analysed.

**🟠 75.2% of all communities are active dumping hotspots** — but not all hotspots are equal. 136 of them are structural hotspots driven by distance from disposal sites, not behavioural failure. Enforcement campaigns will not fix these. Infrastructure access will.

**🟡 106 high-risk communities generate over 15 tons of waste monthly but receive collection only once per week.** Increasing frequency to twice per week is associated with a 35% reduction in illegal dumping — the single highest-return intervention in this dataset, requiring no new infrastructure.

**🟢 Infrastructure quality (r = -0.81) and collection frequency (r = -0.64) are the two strongest predictors of low risk** — more than awareness, economic status, or population density combined.

---

## What Makes This Project Different

### The Recalibration Decision
The original risk classification flagged **841 of 1,000 communities (84.1%) as High Risk** — a number so large it communicates nothing actionable. A policymaker cannot prioritise 841 equally-weighted communities.

I identified this as a calibration failure and rebuilt the classification using a **percentile-based four-tier model**:

| Tier | Threshold | Communities | % of Dataset |
|---|---|---|---|
| 🟢 Low | ≤ 33rd percentile | 330 | 33% |
| 🟡 Medium | ≤ 66th percentile | 330 | 33% |
| 🟠 High | ≤ 85th percentile | 190 | 19% |
| 🔴 Critical | > 85th percentile | 150 | 15% |

The original columns were kept and renamed (not deleted) as an audit trail — because the recalibration story is itself worth showing.

### The Dashboard Design
The Power BI dashboard uses a **clean corporate environmental palette** — soft white canvas, forest green headers, muted risk tier colours — designed specifically for government and NGO stakeholders, not a tech audience. Every colour decision is intentional and documented.

---

## Repository Structure

```
EcoTracK---AI/
├── README.md
├── data/
│   └── EcoTrack_AI_Corrected.xlsx        # Corrected dataset with all computed columns
├── documentation/
│   ├── EcoTrack_AI_Documentation.docx    # Full methodology and decisions log
│   └── EcoTrack_AI_Insights_Recommendations.docx  # Analyst insights report
└── dashboard/
    └── EcoTrack_AI.pbix                  # Power BI dashboard (open in Power BI Desktop)
```

---

## How to Use This Repository

**To explore the dataset:**
Download `EcoTrack_AI_Corrected.xlsx` from the `data` folder and open in Microsoft Excel.

**To view the dashboard:**
Download `EcoTrack_AI.pbix` from the `dashboard` folder and open in [Power BI Desktop](https://powerbi.microsoft.com/desktop) (free download).

**To read the full methodology:**
Download `EcoTrack_AI_Documentation.docx` from the `documentation` folder.

**To read the insights and policy recommendations:**
Download `EcoTrack_AI_Insights_Recommendations.docx` from the `documentation` folder.

---

## Risk Scoring Methodology

```
Risk Score = (0.35 × Dumping) + (0.25 × Drainage) + (0.25 × Flood) + (0.15 × Complaints)
```

All four inputs are **min-max normalised** before weighting — converting each variable to a 0–1 scale so no column dominates due to its raw numeric range.

---

## Dataset Overview

- **1,000 communities** across **12 Nigerian states**
- **22 columns** including 5 computed columns added during analysis
- **Period:** 2023 – 2024
- Synthetic dataset with embedded causal relationships designed to reflect real Nigerian urban environmental conditions

---

## About the Analyst

I am a data analyst in progress — documenting my learning journey from Industrial Chemistry student to data professional.

This project is part of my public portfolio demonstrating applied skills in data analysis, risk modelling, and stakeholder communication.

 Follow the build: [@hey_felicia1](https://www.instagram.com/hey_felicia1) on Instagram

---

*EcoTrack AI · Built by Felicia · June 2026*
