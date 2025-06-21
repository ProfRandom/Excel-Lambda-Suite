# 🔢 Sequence LAMBDA Suite for Excel

This suite provides Excel LAMBDA functions for generating evenly spaced numeric sequences with full control over bounds, count, and step size. These tools are ideal for modeling, simulations, parameter sweeps, or any scenario requiring structured numeric arrays.

---

## 📘 Overview

The functions simplify generating ordered numeric arrays that are often awkward to produce directly in Excel. They handle both fixed-count sequences and flexible dynamic-length sequences with inferred direction, making them highly composable in dynamic spreadsheets.

---

## 📑 Function Index

| Function | Summary |
|---------|---------|
| `SEQ_SPAN` | Generates an evenly spaced sequence between two bounds, given a total count of values (includes both endpoints). |
| `SEQ_STEP` | Generates a sequence from lower to upper bound using a fixed step size (direction auto-inferred). |

---

## 🧩 Highlights and Tips

- 📏 **Fixed Count**: Use `SEQ_SPAN` when you know exactly how many values you want between two endpoints — great for interpolation, graphing, or smooth scales.
- ⚙ **Flexible Step Size**: `SEQ_STEP` lets you generate growing or shrinking sequences based on step size, automatically handling direction.
- 🔀 **Built on SEQUENCE**: Both functions leverage Excel’s native dynamic array behavior for clean integration into modeling pipelines.
- 🧪 **Modeling Friendly**: Especially useful in scientific, engineering, or financial models needing parameter grids or sampling arrays.

---

## ⚙️ Requirements

- ✅ Modern Excel with LAMBDA and dynamic array support (Office 365 or Excel 2021+).
- 🚫 No external dependencies or constant sets required.

---

## 📎 File Contents

- `Sequence Excel LAMBDA Suite.txt`: Master definitions file with inline comments and annotated examples.
- `README.md`: This guide (suitable for GitHub or Obsidian publishing).
# 🔢 Sequence LAMBDA Suite for Excel

This suite provides Excel LAMBDA functions for generating controlled numeric sequences, including evenly spaced ranges, stepped series, repeated values, and bounded arrays. These tools are ideal for simulations, parametric modeling, grid generation, and scalable worksheet design.

---

## 📘 Overview

The suite offers intuitive sequence construction for both fixed-count and step-based generation, with support for repeated values and bounded clamping. All functions leverage Excel's dynamic arrays for highly composable numeric workflows.

---

## 📑 Function Index

| Function | Summary |
|---------|---------|
| `SEQ_SPAN` | Generates a fixed-count evenly spaced sequence between lower and upper bounds, always including both endpoints. |
| `SEQ_STEP` | Generates a dynamic-length sequence using a defined step size, automatically inferring direction. |
| `SEQ_REPEAT` | Produces a sequence where each element is repeated a specified number of times (useful for expansion and sampling). |
| `SEQ_BOUND` | Clamps a given value to the nearest limit within a defined lower and upper bound (bounding helper function). |

---

## 🧩 Highlights and Tips

- 📏 **Evenly Spaced Control**: `SEQ_SPAN` guarantees exact inclusion of both bounds, ideal for interpolation or chart scales.
- ⚙ **Flexible Step Logic**: `SEQ_STEP` dynamically determines sequence direction, handling both positive and negative step sizes.
- 🔁 **Repeating Sequences**: `SEQ_REPEAT` allows controlled repetition of elements for modeling weighted lists, sampling, or visual patterning.
- 🚫 **Safe Bounds Handling**: `SEQ_BOUND` ensures values remain constrained within defined limits, useful in scoring models and safety checks.

---

## ⚙️ Requirements

- ✅ Modern Excel with LAMBDA and dynamic array support (Office 365 or Excel 2021+).
- 🚫 No external dependencies or constant sets required.

---

## 📎 File Contents

- `Sequence Excel LAMBDA Suite.txt`: Master definitions file with inline comments and annotated examples.
- `README.md`: This guide (suitable for GitHub or Obsidian publishing).
