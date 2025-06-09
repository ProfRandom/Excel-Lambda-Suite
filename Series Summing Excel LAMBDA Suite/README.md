# SUM_ Utilities Suite

This suite of Excel LAMBDA functions focuses on summing sequences, arithmetic ranges, and numerically patterned intervals. These utilities are optimized for performance using closed-form expressions and are ideal for applications involving mathematical series, control loops, or range-based analysis.

> See `Summing Utils.txt` for complete logic, usage patterns, and inline documentation.

---

## 🧮 Function Index

| Function Name | Description |
|---------------|-------------|
| `SUM_N_TERMS` | Calculates the sum of an arithmetic progression given a start, length, and step size. |
| `SUM_INTEGERS` | Calculates the sum of all integers, even numbers, or odd numbers from 1 to a specified value. |
| `SUM_RANGE` | Sums values between a lower and upper bound with a defined increment (defaults to 1). |
| `SUM_BETWEEN_BOUNDS` | Sums terms of an arithmetic sequence from a start value up to (but not exceeding) an upper limit, using a fixed increment. |

---

## 📘 Usage Notes

- All functions are built with `LAMBDA` and avoid iterative logic, relying on analytical formulas for efficiency.
- `SUM_RANGE` and `SUM_BETWEEN_BOUNDS` both allow partial inputs and default behaviors (e.g., 1-to-n summation).
- `SUM_INTEGERS` supports selective summation by mode:
  - `0` = all integers (default)
  - `1` = even numbers
  - `2` = odd numbers
- These functions can be composed inside larger dynamic formulas or reporting expressions.

---

## 📂 Files

- `Summing Utils.txt`: Full implementation and commentary for each summation utility.
