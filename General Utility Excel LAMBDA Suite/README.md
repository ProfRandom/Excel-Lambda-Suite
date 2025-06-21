# 🧮 General Utility LAMBDA Suite for Excel

This suite provides a versatile collection of Excel LAMBDA functions for data formatting, strict counting, mathematical operations, and formula inspection. These tools are particularly useful for LAMBDA developers, spreadsheet modelers, and dynamic array workflows where precision, debugging, or composability are required.

---

## 📘 Overview

The suite includes compact utilities for rounding, reciprocals, roots, fractional extraction, formula text retrieval, array formatting for nested LAMBDAs, and strict non-blank counting that excludes logical and error values. These are building-block functions designed to simplify formula chains and make advanced spreadsheets more transparent and reliable.

---

## 📑 Function Index

| Function | Summary |
|---------|---------|
| `FORMAT_AS_LIST` | Formats a range into Excel array constant string syntax, optionally sorted, unique, and styled. |
| `COUNTA_STRICT` | Counts non-blank cells while excluding `FALSE` and error values for stricter dynamic array logic. |
| `FORMULA_TEXT` | Returns the text of a formula from a referenced cell (useful for debugging and auditing models). |
| `ROUND_FIX` | Rounds numbers, but preserves clean integer appearance when no decimals are present. |
| `FRAC` | Returns only the fractional part of a numeric value (portion after the decimal point). |
| `RECIP` | Calculates the reciprocal (`1/x`) of a value, returning `#DIV/0!` style errors safely for zero input. |
| `ROOT` | Computes any nth root of a number with basic error handling for invalid roots or negative inputs. |

---

## 🧩 Highlights and Tips

- 🔧 **LAMBDA Authoring Aid**: `FORMAT_AS_LIST` is especially useful for constructing dynamic LAMBDA constants.
- 🧹 **Strict Counting**: `COUNTA_STRICT` provides better dynamic behavior by ignoring logical and error values.
- 🧮 **Precision Math**: Use `ROUND_FIX`, `FRAC`, `RECIP`, and `ROOT` to simplify various mathematical manipulations in spreadsheets.
- 🪲 **Formula Inspection**: `FORMULA_TEXT` helps when developing or auditing large LAMBDA-based workbooks.

---

## ⚙️ Requirements

- ✅ Modern Excel with LAMBDA and dynamic array support (Office 365 or Excel 2021+).
- 🚫 No external dependencies or constant sets required.

---

## 📎 File Contents

- `General Utility Excel LAMBDA Suite.txt`: Master definitions file with inline comments and annotated examples.
- `README.md`: This guide (suitable for GitHub or Obsidian publishing).
