# PCT_ Interpolation Utilities Suite

A focused collection of Excel LAMBDA functions for percentage-based calculations, including interpolation, extrapolation, remapping, and display rounding. These utilities are ideal for data normalization, visual scaling, and intuitive relative transformations.

> See `pct_utilities.txt` for complete logic, examples, and edge case handling.

---

## 🧮 Function Index

| Function Name | Description |
|---------------|-------------|
| `PCT_OF` | Calculates a given percentage of a value. |
| `PCT_POSITION` | Calculates the relative position of a target value within a range. |
| `PCT_INTERPOLATE` | Calculates a value within or beyond a range using interpolation. |
| `PCT_LBOUND` | Solves for the lower bound given interpolant, upper bound, and percentage. |
| `PCT_UBOUND` | Solves for the upper bound given lbound, interpolant, and percentage. |
| `PCT_REMAP` | Translates a value from one numerical range to its equivalent position in another range |
| `PCT_REMAP_ARRAY` | Remaps a list of interpolated values from one numeric range to another, |

---

## 📘 Usage Notes

- Precision is controlled via an optional argument in each function (defaults to 3 decimal places).
- Input percentages can be whole numbers or decimals; most functions auto-normalize values >1.
- All interpolations are linear unless otherwise specified.
- `PCT_REMAP_ARRAY` supports full-column remapping via spillable `BYROW` logic.
- Most functions do **not clamp** extrapolated results—values outside the expected range are still computed.

---

## 📂 Files

- `pct_utilities.txt`: Full implementation of all `PCT_` LAMBDA functions with in-line documentation.
