# 📋 List Processing LAMBDA Suite for Excel

This suite provides Excel LAMBDA functions for advanced list manipulation, filtering, duplication analysis, string splitting, grid creation, reverse ordering, and list transformations. These tools are ideal for building dynamic models, dashboards, simulations, and data cleaning pipelines directly within Excel.

---

## 📘 Overview

The suite enables flexible creation, reshaping, and filtering of lists and ranges. It includes functions for duplicate detection, list reversal, expansion, collapsing, enumeration, flattening, and converting between text and array formats — all fully compatible with dynamic arrays and LAMBDA chaining.

---

## 📑 Function Index

| Function | Summary |
|---------|---------|
| `LIST_REMOVE_BLANKS` | Removes blank or empty values from single-column lists. |
| `LIST_REMOVE_BLANK_ROWS` | Removes fully blank rows from 2D tables or single-column lists. |
| `LIST_FILTER_WILDCARD` | Filters list items using partial match with wildcards (`*`). |
| `LIST_FILTER_INDEXED` | Filters lists based on matching index positions against a filter array. |
| `LIST_DUPES_TABLE` | Generates a table of duplicate values and their occurrence counts. |
| `LIST_COUNTEACH_MODE` | Returns all unique items along with their counts and the mode(s). |
| `LIST_IS_DISTINCT` | Checks whether all items in a list are distinct. |
| `LIST_ENUMERATE` | Returns paired list of values and their position index numbers. |
| `LIST_WRAP` | Reshapes a 1D list into multiple rows/columns (grid format). |
| `LIST_GRID` | Generates an indexed grid from one or two input lists for Cartesian product-style structures. |
| `LIST_INVERT` | Inverts columns and rows in a table-style array (transpose with structural awareness). |
| `LIST_FORMAT_AS_STRING` | Converts list or array into a compact comma-delimited string for display. |
| `LIST_FROM_STRING` | Converts a comma-delimited string into a proper Excel array. |
| `LIST_REPEAT_VALUES` | Repeats each list element by a specified count for list expansion. |
| `LIST_SEQUENCE_REPEAT` | Expands a sequence where values and repeat counts are paired. |
| `LIST_SPLIT_DIGITS` | Splits numeric values into individual digits as a list. |
| `LIST_COPY_REVERSE` | Reverses the order of a list or array. |
| `LIST_ZIP` | Combines multiple arrays into a "zipped" list of grouped elements. |
| `LIST_N` | Returns the nth element of a list with safe bounds handling. |

---

## 🧩 Highlights and Tips

- 🔄 **Advanced Filtering**: Use `LIST_FILTER_WILDCARD` and `LIST_FILTER_INDEXED` for granular list filtering scenarios.
- 🧮 **Frequency Tables**: `LIST_DUPES_TABLE` and `LIST_COUNTEACH_MODE` generate valuable duplicate analysis tables for data auditing.
- 🔢 **Enumeration & Indexing**: `LIST_ENUMERATE` attaches position numbers for ordered list management.
- ↔ **Reshaping**: `LIST_WRAP`, `LIST_GRID`, and `LIST_INVERT` provide dynamic reshaping for layout control and combinatorial modeling.
- 🔠 **String ↔ Array Conversions**: `LIST_FROM_STRING` and `LIST_FORMAT_AS_STRING` allow smooth transitions between text strings and Excel dynamic arrays.
- ➗ **Digit Splitting**: `LIST_SPLIT_DIGITS` enables per-digit analysis of numeric values.
- 🔃 **List Reversal and Zipping**: `LIST_COPY_REVERSE` and `LIST_ZIP` assist in structural manipulation of multiple arrays for modeling or reporting.

---

## ⚙️ Requirements

- ✅ Modern Excel with LAMBDA and dynamic array support (Office 365 or Excel 2021+).
- 🚫 No external dependencies or constant sets required.

---

## 📎 File Contents

- `List Excel LAMBDA Suite.txt`: Master definitions file with inline comments and annotated examples.
- `README.md`: This guide (suitable for GitHub or Obsidian publishing).
