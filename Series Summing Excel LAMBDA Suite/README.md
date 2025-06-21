# ➕ Series Summing LAMBDA Suite for Excel

This suite provides Excel LAMBDA functions for computing closed-form sums of arithmetic sequences, natural numbers, bounded ranges, and uniform intervals. These tools eliminate the need for generating full arrays when calculating series sums, making modeling and calculation highly efficient for parametric or financial work.

---

## 📘 Overview

The suite includes closed-form solutions for summing natural numbers, evens, odds, arbitrary arithmetic progressions, and bounded range sums. These functions are ideal for academic, financial, statistical, or simulation models that rely on clean series calculations.

---

## 📑 Function Index

| Function | Summary |
|---------|---------|
| `SUM_N_TERMS` | Calculates sum of an arithmetic progression given start, length, and increment; optionally returns final term only. |
| `SUM_INTEGERS` | Calculates sum of natural numbers, evens, or odds up to a specified limit, based on mode selection. |
| `SUM_RANGE` | Calculates the sum of integers between any two inclusive bounds using closed formula (start to end). |
| `SUM_BETWEEN_BOUNDS` | Like `SUM_RANGE`, but validates and corrects bound order automatically (swaps if necessary). |

---

## 🧩 Highlights and Tips

- 🧮 **Closed-Form Sums**: Avoid generating sequences entirely — all sums are calculated directly with algebraic formulas.
- 🔢 **Arithmetic Progressions**: Use `SUM_N_TERMS` for fully flexible start points, steps, and count of terms.
- 🔟 **Natural Number Summing**: `SUM_INTEGERS` handles simple sums of counting numbers or restricts to even/odd subsets.
- 🧱 **Safe Bounds Handling**: `SUM_BETWEEN_BOUNDS` ensures that accidental upper/lower input order does not affect correctness.
- 📊 **Efficient Computation**: Perfect for financial calculations, resource allocations, stair-step models, or parametric cumulative modeling.

---

## ⚙️ Requirements

- ✅ Modern Excel with LAMBDA and dynamic array support (Office 365 or Excel 2021+).
- 🚫 No external dependencies or constant sets required.

---

## 📎 File Contents

- `Series Summing Excel LAMBDA Suite.txt`: Master definitions file with inline comments and annotated examples.
- `README.md`: This guide (suitable for GitHub or Obsidian publishing).
