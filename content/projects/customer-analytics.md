---
title: "CLV Engine for Predictive Customer Analytics"
date: 2026-02-04
description: "Predict 90-day revenue (CLV), explain drivers with SHAP, and optimize marketing budget allocation with an ROI simulator and decision optimization."
summary: "A production-style CLV system: prediction (XGBoost), explainability (SHAP), and prescriptive budget optimization with sensitivity and Monte Carlo risk analysis."
showBreadCrumbs: false
ShowReadingTime: false
ShowWordCount: false
ShowToc: false
showPostNavLinks: false
disableAnchoredHeadings: true
weight: 2
---

---

<div style="text-align:center;">

{{< figure src="/projects/customer/overview.png" title="The Lead Audit Dashboard" caption="A look at the final interface: The dashboard shows real-time processing, lead concentration metrics, and a detailed breakdown of strategic signals for each prospect." >}}

</div>

---

## What problem does this solve?
Most e-commerce teams are reactive - they analyze last month and blast campaigns broadly.
This project turns customer analytics into a **decision engine**:

- **Predict** which customers will generate revenue in the next 90 days
- **Explain** the drivers globally and per-customer (SHAP)
- **Optimize** how to spend a fixed budget for maximum expected uplift (and quantify risk)

---

## What I built (end-to-end)
**Pipeline**
- Generates a realistic customer + transaction dataset (or uses provided CSVs)
- Builds RFM + behavioral features (recency, frequency, monetary, AOV, tenure, inter-purchase time)
- Trains an **XGBoost regressor** to predict 90-day revenue
- Produces evaluation artifacts (metrics + SHAP global importance)

**App**
- Executive dashboard (revenue estimate + model metrics)
- Drivers of customer value (global SHAP)
- Customer explorer (local explanation)
- ROI simulator + decision optimization
- Sensitivity analysis + Monte Carlo risk analysis

---

## Key results (what a recruiter should notice)
- **Top-decile lift ~5x**: the top 10% predicted customers capture ~50% of future revenue (typical CLV “power law” pattern)
- Strong explainability: business-readable drivers (monetary, AOV, frequency, recency, etc.)
- Prescriptive layer: converts predictions into budget decisions (ROI, efficient frontier, risk)

---

## Dashboard walkthrough

### 1) Drivers of Customer Value (Global SHAP)

<div style="text-align:center;">

{{< figure src="/projects/customer/drivers.png" title="The Lead Audit Dashboard" caption="A look at the final interface: The dashboard shows real-time processing, lead concentration metrics, and a detailed breakdown of strategic signals for each prospect." >}}

</div>

<br>

### 2) Customer Explorer (Local explanation)

<div style="text-align:center;">

{{< figure src="/projects/customer/explorer.png" title="The Lead Audit Dashboard" caption="A look at the final interface: The dashboard shows real-time processing, lead concentration metrics, and a detailed breakdown of strategic signals for each prospect." >}}

</div>

<br>

### 3) ROI Simulator & Optimization

<div style="text-align:center;">

{{< figure src="/projects/customer/optimization.png" title="The Lead Audit Dashboard" caption="A look at the final interface: The dashboard shows real-time processing, lead concentration metrics, and a detailed breakdown of strategic signals for each prospect." >}}

</div>

---

## Notes & Limitations
- The model is predictive (correlation), not causal.
- ROI and uplift are assumption-driven simulations → should be validated with A/B tests / RCTs.
- The optimization is only as good as the uplift + cost assumptions.


---

<div style="text-align: center;">

{{< button href="https://github.com/sebastiankindl/customer-analytics" >}}View Code on GitHub{{< /button >}}

</div>

---

## Live demo

{{< app src="https://customer-analytics-engine.streamlit.app/?embed=true" >}}