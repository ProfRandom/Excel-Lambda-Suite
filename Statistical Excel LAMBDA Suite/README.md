# 📊 Statistical LAMBDA Suite for Excel

This suite provides Excel LAMBDA functions for summary statistics, frequency tables, weighted averages, percentile evaluation, distribution modeling, shape diagnostics, and forensic data analysis (including Benford’s Law support). These tools support exploratory data analysis, audit preparation, business reporting, and scientific modeling directly within Excel.

---

## 📘 Overview

The suite delivers full quantile generation, statistical summaries, flexible percentile remapping, frequency analysis, advanced self-weighted averages, error estimation, and Benford distribution modeling. It supports both broad EDA (exploratory data analysis) and specialized compliance or forensic analytics, all fully dynamic-array compatible.

---

## 📑 Function Index

| Function | Summary |
|---------|---------|
| `STAT_QNTILES` | Calculates quantiles or labeled percentile cuts with bin-mode slicing and precision control. |
| `STAT_FREQ_TABLE` | Generates frequency counts for categorical data ranges. |
| `STAT_SUMMARY` | Returns min, max, mean, median, and standard deviation for a numeric dataset. |
| `STAT_MIDRANGE` | Computes midrange (average of min and max). |
| `STAT_MINMAX` | Returns both minimum and maximum values as a paired array. |
| `STAT_STDERR` | Computes standard error of the mean. |
| `STAT_WTD_AVG` | Computes weighted averages using paired value and weight arrays. |
| `STAT_SELF_WTD_AVG` | Computes self-weighted average where each value serves as its own weight. |
| `STAT_PCT_OF_RANGE` | Calculates what percentage of the range a target value represents. |
| `STAT_VALUE_OF_PCT` | Returns the data value corresponding to a given percentile within a dataset. |
| `STAT_PCT_REMAP` | Remaps a target's position from one range onto a new range based on percentile alignment. |
| `STAT_VAL_BRACKET` | Assigns a value into its corresponding percentile bracket using quantile thresholds. |
| `STAT_VOLUME` | Computes volume from width, depth, and height (simple helper utility). |
| `STAT_BENFORD_TABLE` | Returns expected digit frequencies for Benford’s Law analysis (1st-digit forensic test). |
| `STAT_RND_BENFORD` | Generates random samples distributed according to Benford’s Law (for simulation and testing). |
| `STAT_SHAPE` | Reports array dimensions (rows, columns, total size). |
| `STAT_GEO5` | Calculates the 5-number summary (min, Q1, median, Q3, max). |

---

## 🧩 Highlights and Tips

- 🔢 **Full Quantile Control**: Use `STAT_QNTILES`, `STAT_GEO5`, and `STAT_VAL_BRACKET` for quantile slicing, summarization, and percentile bracketing.
- 🏷 **Frequency Analysis**: `STAT_FREQ_TABLE` generates fast category counts for tables and dashboards.
- 📊 **Summary Statistics**: `STAT_SUMMARY`, `STAT_MINMAX`, `STAT_MIDRANGE`, and `STAT_STDERR` deliver instant descriptive statistics.
- 🎯 **Percentile Mapping**: `STAT_PCT_OF_RANGE`, `STAT_VALUE_OF_PCT`, and `STAT_PCT_REMAP` allow seamless value-position scaling across ranges.
- ⚖ **Weighted Averaging**: Support both external (`STAT_WTD_AVG`) and self-weighted (`STAT_SELF_WTD_AVG`) averages for flexible scoring models.
- 🧪 **Benford Forensics**: `STAT_BENFORD_TABLE` and `STAT_RND_BENFORD` offer forensic tools for compliance auditing and fraud detection.
- 🧬 **Shape Diagnostics**: `STAT_SHAPE` helps LAMBDA authors diagnose dynamic array dimensions for robust formula design.

---

## ⚙️ Requirements

- ✅ Modern Excel with LAMBDA and dynamic array support (Office 365 or Excel 2021+).
- 🚫 No external dependencies or constant sets required.

---

## 📎 File Contents

- `Stastistical Excel LAMBDA Suite.txt`: Master definitions file with inline comments and annotated examples.
- `README.md`: This guide (suitable for GitHub or Obsidian publishing).
