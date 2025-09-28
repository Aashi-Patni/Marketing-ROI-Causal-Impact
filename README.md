
# Causal Impact Analysis of Sponsored Search Ads for Bazaar.com

## 🧠 Project Summary

This project investigates the **true return on investment (ROI)** of branded sponsored search ads on Bazaar.com using **causal inference techniques**. A natural experiment occurred when Google ads were unintentionally paused, enabling a **Difference-in-Differences (DiD)** analysis to isolate **incremental ad effects** versus organic traffic cannibalization.

---

## 💼 Business Value

While traditional ROI calculations often assume that all paid traffic is incremental, this project corrects such overestimates by quantifying **causal impact**. The refined ROI estimate shows a **realistic 241% return**, in contrast to the **inflated 320% originally claimed** by the marketing team.

This provides decision-makers with:
- A **clearer understanding of true ad effectiveness**
- Evidence for **budget reallocation and attribution refinement**
- A framework to **scale causal modeling** in digital marketing analytics

---

## 🔬 Analytical Approach

| Step | Description |
|------|-------------|
| **1. Problem Framing** | Identified flaw in naive ROI assumption that all sponsored clicks are incremental |
| **2. Data Cleaning** | Removed duplicates, verified missing values, and created new variables for traffic |
| **3. Exploratory Data Analysis** | Visualized weekly traffic and distribution of total visits |
| **4. First Difference Model** | Found that a simple before/after model lacked statistical power |
| **5. Difference-in-Differences (DiD)** | Used Google (treatment) vs. Bing/Yahoo/Ask (control) across 12 weeks |
| **6. Parallel Trends Validation** | Checked using visual plots and a dynamic DiD model |
| **7. Adjusted ROI Calculation** | Derived ROI based on incremental clicks only |

---

## 🧪 Experiment Design

- **Natural Experiment Trigger**: Google sponsored ads stopped during weeks 10–12 due to a technical issue
- **Unit of Observation**: Platform-week (e.g., Google in Week 9)
- **Treatment Group**: Google during weeks 10–12
- **Control Group**: Bing, Yahoo, Ask across all 12 weeks

---

## 🧮 Key Findings

| Metric | Value |
|--------|-------|
| Estimated traffic loss per week (Google post-treatment) | **-9,911** clicks |
| Portion of incremental clicks | **~81%** |
| Adjusted ROI | **241%** |
| Original (flawed) ROI | **320%** |
| Corrected Impact | Ads truly drove only ~80% of their claimed traffic |

---

## 📈 Visualizations

- **Total Traffic Trends** across platforms
- **Histogram & Density Plots** for weekly visits
- **Pre-treatment vs. Post-treatment Trajectories**
- **Dynamic DiD Event Study**

---

## 📌 Tools & Libraries Used

### 🔧 Languages & Environment
- **RMarkdown** (`.Rmd`)
- **R Language**

### 📦 R Libraries
- `dplyr` – data wrangling  
- `ggplot2` – data visualization  
- `readr` – CSV parsing  
- `stats` – regression modeling

### 🖥️ Tools
- **RStudio** – development environment  

---

## 📂 Dataset

**did_sponsored_ads.csv** – includes 48 rows covering:
- 4 platforms × 12 weeks
- Variables: `platform`, `week`, `avg_spons`, `avg_org`, `total_traffic`

---

## ✅ Recommendations to Management

1. **Continue Branded Ads**, but with ROI expectations based on causal impact.
2. **Optimize Ad Timing** based on behavioral data.
3. **Implement Controlled Experiments** (geo-tests, A/B testing).
4. **Shift to Causal Attribution** models for better budgeting.

---
