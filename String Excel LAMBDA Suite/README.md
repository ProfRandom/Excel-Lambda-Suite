# STR_ String Utilities Suite

A robust set of Excel LAMBDA functions designed for string manipulation, character filtering, and lightweight text parsing. These utilities are essential for cleaning input, analyzing character composition, and building custom transformation pipelines inside spreadsheets.

> See `str_utilities.txt` for the full implementation, notes, and examples.

---

## 🧮 Function Index

| Function Name | Description |
|---------------|-------------|
| `STR_GETDIGITS` | Extracts all digit characters (0–9) from a text string and returns them as a single string. |
| `STR_GETCHARS` | Extracts all non-digit characters from a text string and returns them as a single string. |
| `STR_FILTERCHARS` | Filters characters from a string based on a named mode (e.g., digits, letters, symbols). |
| `STR_SANITIZE` | Replaces invisible or nonstandard whitespace characters with ASCII space. |
| `STR_SPLITCHARS` | Splits a string into individual characters as a column or row array. |
| `STR_UNIQUECHARS` | Returns the unique characters from a string, with optional case normalization and sorting. |
| `STR_HASCAP_AFTERFIRST` | Returns TRUE if a string contains a capital letter after the first character. |
| `STR_TEXTBETWEEN` | Extracts the substring between two delimiters. |
| `STR_REMOVE_ENCLOSED` | Recursively removes all text inside parentheses, including the parentheses themselves. |
| `STR_COUNTCHAR` | Counts how many times a given character appears in a string. |

---

## 📘 Usage Notes

- All functions are Excel-native and use `LAMBDA` syntax; compatible with dynamic arrays and `LET`.
- Fallback values like `"#NONE!"` can be overridden in most extraction functions.
- Functions like `STR_FILTERCHARS` and `STR_UNIQUECHARS` include case handling, ASCII evaluation, or mode selectors.
- Designed to complement each other—e.g., `STR_SANITIZE` → `STR_GETCHARS` → `STR_UNIQUECHARS` is a useful pipeline.

---

## 📂 Files

- `str_utilities.txt`: Source file with full inline documentation and code examples.
