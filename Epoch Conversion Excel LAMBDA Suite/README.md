# Epoch Conversion Excel LAMBDA Suite

This suite contains Excel LAMBDA functions that convert between Unix-style epoch time formats (seconds, milliseconds, etc.) and standard Excel date-time serial values.

Epoch time is widely used in computing as the number of seconds since 1970-01-01 00:00:00 UTC ("the Unix epoch"). Excel’s internal date serial system uses 1900-01-01 as its base (serial value 1), making conversion between the two essential when handling time data across systems.

---

## Included Functions

### ✅ `EPOCH_SECONDS_TO_SERIAL`
**Converts epoch seconds to Excel serial date-time.**

- Input: Number of seconds since 1970-01-01 00:00:00 UTC.
- Output: Excel-compatible serial date-time.

---

### ✅ `EPOCH_MILLIS_TO_SERIAL`
**Converts milliseconds since epoch to Excel serial.**

- Input: Number of milliseconds since 1970-01-01 00:00:00 UTC.
- Output: Excel-compatible serial date-time.

---

### ✅ `EPOCH_SERIAL_TO_SECONDS`
**Converts Excel serial to epoch seconds.**

- Input: Excel serial date-time.
- Output: Number of seconds since 1970-01-01 00:00:00 UTC.

---

### ✅ `EPOCH_SERIAL_TO_MILLIS`
**Converts Excel serial to epoch milliseconds.**

- Input: Excel serial date-time.
- Output: Number of milliseconds since 1970-01-01 00:00:00 UTC.

---

### ✅ `EPOCH_OFFSET_DAYS`
**Returns the number of Excel serial days between Excel's base date and the Unix epoch.**

- Constant function.
- Output: 25569

---

## Usage Notes

- These functions account for the offset between Excel and Unix epoch bases (25569 days).
- Can be used in either UTC or local time depending on your system time interpretation.
- Useful when importing/exporting time data to/from databases, APIs, or JSON logs.

---

## Status

This suite is complete and production-ready. No external dependencies.

