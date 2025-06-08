# LIST_ Utilities Suite

A comprehensive collection of Excel LAMBDA functions for list manipulation, filtering, formatting, and transformation. These functions offer high-performance, declarative approaches to common list-processing tasks in spreadsheets.

> See `list_utilities.txt` for full function definitions and usage examples.

---

## 🧮 Function Index

| Function Name | Description |
|---------------|-------------|
| `LIST_REMOVE_BLANKS` | Removes blank or empty values from a vertical list (single-column range or array). |
| `LIST_REMOVE_BLANK_ROWS` | Removes fully blank rows from a 2D table (or single-column list). |
| `LIST_FILTER_WILDCARD` | Filters items from an array using a partial match string (with or without wildcards). |
| `LIST_DUPES_TABLE` | Returns a two-column array of values that appear more than once in a list, |
| `LIST_COUNTEACH_MODE` | Counts how many times each unique item appears in the list. |
| `LIST_FORMAT_AS_STRING` | Formats a list as a delimited string with optional control over uniqueness, sorting, and braces. |
| `LIST_COPY_REVERSE` | Reverses a list vertically (default) or horizontally using keyword-based mode input. |
| `LIST_REPEAT_VALUES` | Repeats each item in a given list a fixed number of times, in order. |
| `LIST_SEQUENCE_REPEAT` | Creates a numeric sequence from start to end, repeating each number a specified number of times. |
| `LIST_SPLIT_DIGITS` | Extracts all digit characters (0–9) from a text string and returns them as a numeric array. |
| `LIST_FROM_STRING` | Converts a delimited text string into a list (vertical or horizontal array). |
| `LIST_ENUMERATE` | Returns a two-column array pairing each item in a list with its index. |
| `LIST_ZIP` | Combines two lists into a two-column array, pairing elements by position. |
| `LIST_GRID` | Returns the Cartesian product of two lists as a two-column array, |
| `LIST_INVERT` | Flips a 2D table by rows, columns, or both (mirror-like inversion). |
| `LIST_WRAP` | Rotates a list by N positions with wraparound, preserving all values. |
| `LIST_N` | Returns a list of a single repeated value. |
| `LIST_FILTER_INDEXED` | Returns items from a list based on a list of index positions (1-based). |
| `LIST_IS_DISTINCT` | Returns TRUE if all values in the list are unique (no duplicates), FALSE otherwise. |

---

## 📘 Usage Notes

- All functions are pure LAMBDA constructs with no external dependencies.
- Most functions operate on vertical lists but support horizontal or 2D variants as noted.
- Functions are composable—many are designed to work well together (e.g., `LIST_ENUMERATE` + `LIST_FILTER_INDEXED`).
- Output orientation is often controllable via optional parameters (e.g., `mode=1` for horizontal).
- Supports use cases in text cleanup, data normalization, display formatting, and more.

---

## 📂 Files

- `list_utilities.txt`: Full source code for all `LIST_` LAMBDA functions with inline documentation.
