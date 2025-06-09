# 🛠️ General Utility Excel LAMBDA Suite

This suite includes essential Excel LAMBDA functions that serve a broad range of use cases: numeric manipulation, rounding, formula introspection, formatting, and strict counting. These are reusable primitives across multiple domains.

All functions are compatible with Excel 365+ and support spill-aware behavior.

---

## ✅ Included Functions

### `FORMAT_AS_LIST`
**Converts a range or array into a valid Excel array constant string.**

- Format: `{a, b, c}` (horizontal) or `{a; b; c}` (vertical)
- Optional flags for format, style, sorting, and uniqueness
- Used in embedding lists into LAMBDAs

---

### `RECIP`
**Returns the reciprocal (1 divided by input).**

- Simple inversion
- Returns `#DIV/0!` if input is zero

---

### `FRAC`
**Returns the fractional part of a number.**

- Optional `mode`:  
  - `0`: always positive (default)  
  - `1`: preserves sign (e.g., -3.25 → -0.25)

---

### `ROOT`
**Computes the x-th root of a number.**

- Defaults to square root
- Returns `#NUM!` for negative bases

---

### `FORMULA_TEXT`
**Displays the formula in a cell as a labeled string.**

- Output: `"A1:= formula"`  
- Strips the equal sign and prepends cell reference
- For teaching, auditing, or dashboards

---

### `ROUND_FIX`
**Truncates or rounds a number to fixed decimal places.**

- Optional `as_text` flag to preserve trailing zeroes
- Optional `use_round` flag for true rounding vs truncation
- Numeric output capped at 9 digits for Excel compatibility

---

### `COUNTA_STRICT`
**Counts non-empty, non-whitespace cells in a range.**

- Ignores `""`, `" "`, and blank values
- Useful when trimming user-entered lists

---

## 🔧 Utility Focus

These functions were selected for their wide applicability and minimal dependencies. Ideal for general-purpose modeling, teaching, and composing higher-order LAMBDAs.

---

## 📁 File

`General Utility Excel LAMBDA Suite.txt`
