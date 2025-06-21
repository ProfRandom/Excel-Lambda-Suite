# 📊 Percentage LAMBDA Suite for Excel

This suite provides Excel LAMBDA functions for flexible percentage calculations, range normalization, interpolation, scaling, and bidirectional remapping. These tools simplify percentile workflows for modeling, grading systems, dashboards, and dynamic scaling tasks in Excel.

---

## 📘 Overview

The suite allows users to work seamlessly with percentage-based calculations, including relative positioning within ranges, bidirectional remapping between different value domains, percent-based interpolation, and bound resolution for complex scoring or scaling systems.

---

## 📑 Function Index

| Function | Summary |
|---------|---------|
| `PCT_OF` | Calculates a percentage of a value, accepting decimal or whole-number percent inputs. |
| `PCT_POSITION` | Calculates the relative position of a target value within a min-max range (returns a 0–1 scale). |
| `PCT_REMAP` | Remaps a target’s position from one range to a corresponding value in a different output range. |
| `PCT_REMAP_ARRAY` | Applies `PCT_REMAP` to arrays of values for dynamic range remapping across datasets. |
| `PCT_RESOLVE` | Attempts to automatically resolve partial percent input into valid proportions (e.g., 0.75 vs 75). |
| `PCT_LBOUND` | Returns the lower bound (0%) value from a defined range structure. |
| `PCT_UBOUND` | Returns the upper bound (100%) value from a defined range structure. |
| `PCT_INTERPOLATE` | Calculates interpolated values between two percent/value pairs (useful for scoring rubrics or partial grading). |

---

## 🧩 Highlights and Tips

- 🔢 **Flexible Percent Input**: `PCT_OF` and `PCT_RESOLVE` accept both decimal and whole-number percentages, reducing input errors.
- 📈 **Range Positioning**: `PCT_POSITION` converts values into normalized scales for grading, weighting, or visual gauges.
- 🔄 **Dynamic Scaling**: `PCT_REMAP` and `PCT_REMAP_ARRAY` allow rescaling between arbitrary input/output domains, great for scoring models.
- 📊 **Interpolation Logic**: `PCT_INTERPOLATE` allows for multi-point percent-based grading or scoring interpolation.
- 🔧 **Bound Access**: `PCT_LBOUND` and `PCT_UBOUND` extract range limits for downstream model calculations.

---

## ⚙️ Requirements

- ✅ Modern Excel with LAMBDA and dynamic array support (Office 365 or Excel 2021+).
- 🚫 No external dependencies or constant sets required.

---

## 📎 File Contents

- `Percentage Excel LAMBDA Suite.txt`: Master definitions file with inline comments and annotated examples.
- `README.md`: This guide (suitable for GitHub or Obsidian publishing).
