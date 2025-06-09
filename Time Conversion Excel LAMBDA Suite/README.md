# TIME_ Utilities Suite

This suite contains versatile and powerful Excel LAMBDA functions for manipulating, converting, formatting, and computing with time values. The functions handle both numeric and textual inputs, support multiple unit systems (Y/D/H/M/S), and offer formatting suitable for display or downstream computation.

> See `time_utils.txt` for full function definitions, comments, and usage examples.

---

## 🧮 Function Index

| Function Name | Description |
|---------------|-------------|
| `TIME_UNITS_TO_DECIMAL` | Converts structured time components (Y/D/H/M/S) into a single decimal value in the specified unit. |
| `TIME_DECIMAL_TO_UNITS` | Converts a decimal duration (in Y/D/H/M/S) into a human-readable or formatted breakdown string. |
| `TIME_DIFF` | Computes the time difference between two Excel time values and returns it in multiple formats. |
| `TIME_MIL12_TO_MIL24` | Converts "military-style" 12-hour strings (e.g., `"0930AM"`) into standard 24-hour format (`"HHMM"`). |
| `TIME_MIL24_TO_MIL12` | Converts 24-hour military time (`"HHMM"`) into compact 12-hour format (`"hhmmAM/PM"`). |
| `TIME_MIL12_TO_CLOCK12` | Converts compact military 12-hour strings into display-friendly `"h:mmAM"` or `"h:mmPM"` formats. |
| `TIME_CLOCK12_TO_MIL12` | Converts Excel-style `"h:mm AM"` strings into compact `"hhmmAM"` military format. |
| `TIME_MIL12_SHIFT` | Shifts a `"hhmmAM"` style time by a specified number of hours (positive or negative). |
| `TIME_STD12_SHIFT` | Shifts a standard 12-hour Excel time by fractional hours, with optional formatted output. |

---

## 📘 Usage Notes

- **Serial vs. Text**: Many functions accept or return Excel serial times, while others use compact string formats.
- **Flexible Units**: `TIME_UNITS_TO_DECIMAL` and `TIME_DECIMAL_TO_UNITS` use astronomical year assumptions (365.25 days).
- **Display Optimization**: Output formatting is compatible with dashboards, logs, and printable reports.
- **Time Wrapping**: Functions like `TIME_MIL12_SHIFT` and `TIME_STD12_SHIFT` gracefully wrap around midnight using modulo logic.
- **Error Handling**: Most conversions return readable fallback strings like `"Invalid Unit"` or `"Invalid Input"` when inputs are malformed.

---

## 📂 Files

- `time_utils.txt`: Full suite with function definitions, inline documentation, and examples.
