# 🥗 Obesity & Dietary Habits Analysis — Latin American Population

> Analyzed a dataset of 2,111 records — sourced from a real survey conducted in Mexico, Peru, and Colombia, and augmented with synthetically generated data using the SMOTE algorithm — to explore the relationship between dietary habits, physical activity, age, and obesity levels.

---

## 📋 Project Overview

This project was developed as part of a data analytics portfolio. It follows the complete workflow of a data analyst: obtaining data from a public source, cleaning and documenting it, analyzing it through visualizations, and communicating findings in a structured report.

**Business Questions:**
- Which dietary and lifestyle habits are most associated with higher obesity levels?
- Are there significant differences in obesity distribution between genders?
- How does obesity prevalence vary across age groups?
- What percentage of the population meets basic healthy habit thresholds?

---


## 📊 Dataset

| Detail | Info |
|--------|------|
| **Source** | UCI Machine Learning Repository |
| **URL** | https://archive.ics.uci.edu/dataset/544 |
| **License** | CC BY 4.0 |
| **Countries** | Mexico, Peru & Colombia |
| **Records** | 2,111 rows × 17 original columns |
| **Synthetic data** | 77% generated via SMOTE algorithm |

---

## 🔧 Data Cleaning Process

All cleaning was performed in **Microsoft Excel**. The original raw file was preserved without modifications.

| Step | Action |
|------|--------|
| Synthetic data identification | Detected decimal values in ordinal columns (e.g., FCVC = 2.341) — documented as dataset characteristic |
| Ordinal scale rounding | Rounded FCVC, NCP, CH2O, FAF, TUE to integer using `=ROUND(cell, 0)` |
| BMI calculation | Added column: `=Weight/(Height*Height)` |
| Age group segmentation | Created Age_Group using nested IF: Under_18, 19–25, 26–35, 36+ |
| Null value check | Confirmed 0 null values across all columns |

**Engineered columns added:** `BMI`, `Age_Group`
**Final dataset:** 2,111 rows × 19 columns

---

## 📈 Key Findings

### Finding 1 — Physical Activity & Obesity Level
The Obesity_Type_III group shows the lowest physical activity average (FAF) across the entire sample. A clear inverse relationship exists between physical activity frequency and obesity level — the more active a person is, the closer they tend to be to a healthy weight.

### Finding 2 — Gender Distribution Across Obesity Types
Obesity_Type_III is represented almost entirely by women, while Obesity_Type_II is nearly 100% male (only 2 female cases). These differences are too large to be explained by biology alone and likely reflect a bias introduced by the SMOTE data generation process.

### Finding 3 — Obesity by Age Group
The 36+ group shows proportionally more obesity despite being the smallest segment (168 participants). Three factors may explain this: reduced physical activity, less balanced dietary patterns, and decreased basal metabolic rate — a well-documented physiological change in adults over 35.

---

## ⚠️ Limitations

- 77% of records are synthetically generated (SMOTE), which may produce unrealistic correlations
- Ordinal scales (1–3) limit measurement precision vs. continuous clinical measurements
- Sample is biased toward young university students (53% aged 19–25)
- NObeyesdad classification does not directly correspond to standard WHO BMI ranges
- Self-reported dietary data tends to overestimate healthy behaviors

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| Microsoft Excel | Data cleaning, pivot tables, exploratory analysis |
| Power BI Desktop | Interactive dashboard with cross-filtering slicers |

---

## 👤 Author

**Emanuel Vaglio**
Data Analytics Portfolio — May 2025

---

*This project is part of an ongoing portfolio demonstrating data cleaning, analysis, and visualization skills.*
