# 🔢 Number Notation LAMBDA Suite for Excel

This suite provides Excel LAMBDA functions for converting numbers into specialized notations, including engineering formats, SI-style magnitude suffixes, and tagged exponential formats. These tools are helpful for scientific modeling, dashboards, reports, or any situation where compact and readable numeric display improves interpretation.

---

## 📘 Overview

The suite offers controlled precision formatting for technical presentations, simulation outputs, or scientific summaries. All functions support clean string outputs with customizable precision, aligned to standard engineering and scientific practices.

---

## 📑 Function Index

| Function | Summary |
|---------|---------|
| `NUMNOTE_ENGINEERING` | Converts a number into engineering notation where exponents are multiples of 3 (e.g., `1.23E+06`). |
| `NUMNOTE_MAGNITUDE` | Converts numbers into human-readable SI-style magnitude suffixes (e.g., k, M, G, m, μ, n). |
| `NUMNOTE_POWERTAG` | Converts numbers into explicit exponential power tags (e.g., `1.23×10^6`) for publication-quality formatting. |

---

## 🧩 Highlights and Tips

- ⚙ **Engineering Alignment**: `NUMNOTE_ENGINEERING` ensures that exponents align with common SI engineering units (multiples of 3).
- 🔠 **Compact Suffixing**: `NUMNOTE_MAGNITUDE` is ideal for dashboards and summary tables where compact presentation improves readability.
- 🧪 **Scientific Formatting**: `NUMNOTE_POWERTAG` produces true scientific-style exponential formatting useful for printed reports, papers, or educational materials.
- 🔧 **Precision Control**: All functions allow you to specify the number of decimal places for clean numeric presentation.

---

## ⚙️ Requirements

- ✅ Modern Excel with LAMBDA and dynamic array support (Office 365 or Excel 2021+).
- 🚫 No external dependencies or constant sets required.

---

## 📎 File Contents

- `Number Notation Excel LAMBDA Suite.txt`: Master definitions file with inline comments and annotated examples.
- `README.md`: This guide (suitable for GitHub or Obsidian publishing).
