# NUMNOTE Utilities Suite

A small but powerful collection of Excel LAMBDA functions for numeric display formatting in scientific, engineering, and magnitude-aware contexts. These functions provide precision control and clarity for metrics, charts, dashboards, or reports.

> See `numnote_utilities.txt` for full source code and usage examples.

---

## 🧮 Function Index

| Function Name | Description |
|---------------|-------------|
| `NUMNOTE_ENGINEERING` | Converts a number into **engineering notation** (i.e., exponent is always a multiple of 3). |
| `NUMNOTE_MAGNITUDE` | Converts a numeric value into a human-readable string using |
| `NUMNOTE_POWERTAG` | Returns only the exponent tag portion of a number’s scientific or power-of-ten notation. |

---

## 📘 Usage Notes

- Ideal for scientific reporting, engineering dashboards, and annotation layers.
- Precision and format are customizable for each function.
- Outputs are text-formatted strings for clean display.
- `NUMNOTE_MAGNITUDE` and `NUMNOTE_ENGINEERING` differ mainly in how they express exponent scales (metric vs base-10 × 3).
- `NUMNOTE_POWERTAG` is useful as a standalone scale label or combined with values.

---

## 📂 Files

- `numnote_utilities.txt`: Full function listing with inline documentation and examples.
