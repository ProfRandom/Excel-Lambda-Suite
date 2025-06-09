# 📋 List Excel LAMBDA Suite

This suite provides extensive tools for list manipulation in Excel, leveraging LAMBDA functions to clean, enumerate, combine, filter, transform, and validate lists of data. Functions are designed to work with both vertical and horizontal arrays, handle delimited strings, and generate list structures useful in modeling, data preparation, and analysis.

---

## ✅ Included Functions

### `LIST_REMOVE_BLANKS`
Removes empty values (`""`) from a single-column list.

---

### `LIST_REMOVE_BLANK_ROWS`
Removes rows where all cells are empty or whitespace.

---

### `LIST_FILTER_WILDCARD`
Filters list items using partial, starting, or wildcard-based matching.  
Supports three modes of matching (contains, starts with, wildcard).

---

### `LIST_DUPES_TABLE`
Returns a `{value, count}` table of only duplicate values (count > 1).

---

### `LIST_COUNTEACH_MODE`
Counts all items in a list with flexible output:
- Sorted by label or frequency
- Output as pairs, labels only, or counts only

---

### `LIST_FORMAT_AS_STRING`
Formats a list as a delimited string, with control over:
- Uniqueness
- Sorting
- Wrapping in braces

---

### `LIST_COPY_REVERSE`
Reverses a list vertically (default) or horizontally using optional flags.

---

### `LIST_REPEAT_VALUES`
Repeats each list item a set number of times in sequence.

---

### `LIST_SEQUENCE_REPEAT`
Generates a repeated numeric sequence, e.g., 1 1 2 2 3 3.

---

### `LIST_SPLIT_DIGITS`
Extracts all digit characters (0–9) from a string and returns a numeric array.

---

### `LIST_FROM_STRING`
Splits a string by a delimiter into a vertical or horizontal list.

---

### `LIST_ENUMERATE`
Generates a two-column list of `{index, value}` pairs.

---

### `LIST_ZIP`
Pairs two lists by position into a two-column output.  
Supports `"PAD"` (default) or `"TRC"` mode for equalizing lengths.

---

### `LIST_GRID`
Returns the Cartesian product of two lists as a two-column combination table.

---

### `LIST_INVERT`
Flips a 2D table:
- By rows (`"ROWS"`)
- By columns (`"COLS"`)
- Or both (`"BOTH"`)

---

### `LIST_WRAP`
Circularly rotates a list by N positions (positive or negative).

---

### `LIST_N`
Generates a list of a single repeated value with vertical or horizontal orientation.

---

### `LIST_FILTER_INDEXED`
Returns values from a list using an index array.

---

### `LIST_IS_DISTINCT`
Returns `TRUE` if all values are unique; otherwise `FALSE`.

---

## 📘 Notes

- All functions are spill-compatible and Excel 365+ optimized.
- Most accept vertical, horizontal, or full-table ranges.
- Complementary to the **String**, **Sequence**, and **General Utility** suites.

---

Let me know when you're ready for the next suite!
