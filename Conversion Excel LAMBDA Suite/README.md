# 📏 Unit Conversion LAMBDA Suite for Excel

This suite provides a compact set of Excel LAMBDA functions for common temperature conversions and imperial unit formatting. The tools are designed for data modeling, reporting, construction planning, cabinetry layouts, and any workflow where practical unit conversions are required.

---

## 📘 Overview

Each function is self-contained, providing flexible rounding, customizable formatting, and clean handling of fractional inch formats. The suite allows numeric outputs for further calculations or text outputs for direct display in spreadsheets and dashboards.

---

## 📑 Function Index

| Function | Summary |
|---------|---------|
| `CONVERT_TEMP_C_TO_F` | Converts Celsius to Fahrenheit with optional rounding precision. |
| `CONVERT_TEMP_F_TO_C` | Converts Fahrenheit to Celsius with optional rounding precision. |
| `FORMAT_FEET_AND_INCHES` | Converts decimal feet into formatted feet-and-inches strings, supporting decimal or fractional inches. |
| `FORMAT_INCH_FRACTION` | Converts decimal inches into simplified fractional inch format as text. |

---

## 🧩 Highlights and Tips

- 🌡 **Temperature Conversions**: `CONVERT_TEMP_C_TO_F` and `CONVERT_TEMP_F_TO_C` handle both simple and precision-controlled temperature transformations.
- 📏 **Feet-Inches Formatting**: `FORMAT_FEET_AND_INCHES` supports both decimal and fractional inch output for construction-friendly reporting.
- 📐 **Fraction Simplification**: `FORMAT_INCH_FRACTION` automatically reduces inch fractions to lowest terms for clean, human-readable output.
- 🔧 **Flexible Precision**: Decimal rounding precision can be specified for cleaner presentation without extra formatting layers.

---

## ⚙️ Requirements

- ✅ Modern Excel with LAMBDA and dynamic array support (Office 365 or Excel 2021+).
- 🚫 No external dependencies or constant sets required.

---

## 📎 File Contents

- `Conversion Excel LAMBDA Suite.txt`: Master definitions file with inline comments and annotated examples.
- `README.md`: This guide (suitable for GitHub or Obsidian publishing).
