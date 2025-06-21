# ⏱️ Time Conversion LAMBDA Suite for Excel

This suite provides Excel LAMBDA functions for working with mixed time units, clock formats, decimal conversions, and offset calculations. The tools support both interval-based time modeling and 12-hour / 24-hour clock format transformations, useful for scheduling, planning, simulation, and display formatting directly within Excel.

---

## 📘 Overview

The suite enables flexible conversion between component-based time (years, days, hours, minutes, seconds), decimalized time values, and various 12-hour and 24-hour clock formats. Full bidirectional conversion and precise offset handling are supported for complex modeling.

---

## 📑 Function Index

| Function | Summary |
|---------|---------|
| `TIME_UNITS_TO_DECIMAL` | Converts multiple time components (years, days, hours, minutes, seconds) into a decimal time value in any unit (Y, D, H, M, S). |
| `TIME_DECIMAL_TO_UNITS` | Decomposes a decimal time value back into its full component breakdown. |
| `TIME_DIFF` | Calculates the full difference between two decimal time values, returning signed and absolute unit deltas. |
| `TIME_CLOCK12_TO_MIL12` | Converts 12-hour clock time (e.g. `10:30 PM`) to 12-hour military format (0000–1159). |
| `TIME_MIL12_TO_CLOCK12` | Converts 12-hour military time (0000–1159) back to standard 12-hour AM/PM clock format. |
| `TIME_MIL12_TO_MIL24` | Converts 12-hour military format to 24-hour military format (0000–2359). |
| `TIME_MIL24_TO_MIL12` | Converts 24-hour military format back to 12-hour military format. |
| `TIME_MIL12_SHIFT` | Applies offset to 12-hour military time with wraparound adjustment. |
| `TIME_STD12_SHIFT` | Applies offset to standard 12-hour AM/PM clock time with wraparound correction. |

---

## 🧩 Highlights and Tips

- 🔢 **Mixed-Unit Conversion**: Combine `TIME_UNITS_TO_DECIMAL` and `TIME_DECIMAL_TO_UNITS` for clean back-and-forth translations between full time components and decimal forms.
- ⏳ **Precise Differences**: `TIME_DIFF` returns both full-unit breakdown and absolute time difference calculations.
- 🕰 **Clock Format Transformations**: Easily swap between standard clock and military formats using `TIME_CLOCK12_TO_MIL12`, `TIME_MIL12_TO_CLOCK12`, and related functions.
- 🔄 **Offset Adjustments**: Use `TIME_MIL12_SHIFT` and `TIME_STD12_SHIFT` for scheduled adjustments, shift calculations, and circular time modeling.
- 📊 **Simulation-Friendly**: Clean integration with LAMBDA chains for complex time-driven spreadsheet models.

---

## ⚙️ Requirements

- ✅ Modern Excel with LAMBDA and dynamic array support (Office 365 or Excel 2021+).
- 🚫 No external dependencies or constant sets required.

---

## 📎 File Contents

- `Time Conversion Excel LAMBDA Suite.txt`: Master definitions file with inline comments and annotated examples.
- `README.md`: This guide (suitable for GitHub or Obsidian publishing).
