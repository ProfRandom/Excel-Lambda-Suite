# 🔤 String Processing LAMBDA Suite for Excel

This suite provides Excel LAMBDA functions for advanced string parsing, character filtering, extraction, sanitization, and pattern isolation. These tools simplify text preprocessing, cleanup, validation, and transformation directly within spreadsheets — ideal for dynamic models, import pipelines, form processing, and text-heavy data sources.

---

## 📘 Overview

The suite offers powerful string operations that allow you to extract digits, isolate characters, sanitize text, validate casing patterns, split strings into individual characters, and remove enclosed substrings. Fully compatible with dynamic arrays, the functions can be chained for complex text manipulation scenarios.

---

## 📑 Function Index

| Function | Summary |
|---------|---------|
| `STR_GETDIGITS` | Extracts all digit characters from a text string. |
| `STR_GETCHARS` | Extracts all non-digit characters from a text string. |
| `STR_FILTERCHARS` | Filters string content, returning only characters matching a custom character set. |
| `STR_COUNTCHAR` | Counts occurrences of a specific character within a string. |
| `STR_UNIQUECHARS` | Returns unique characters from a string, eliminating duplicates. |
| `STR_SPLITCHARS` | Splits a string into an array of single characters. |
| `STR_HASCAP_AFTERFIRST` | Tests if a string contains capital letters after the first character (camelCase detection). |
| `STR_REMOVE_ENCLOSED` | Removes substrings enclosed within specified start/end markers (e.g., parentheses). |
| `STR_SANITIZE` | Removes control characters (tabs, line breaks, non-printables) from text. |
| `STR_TEXTBETWEEN` | Extracts substring located between two delimiters (simplified version of Excel's native `TEXTBETWEEN`). |

---

## 🧩 Highlights and Tips

- 🔢 **Digit Isolation**: `STR_GETDIGITS` pulls out numeric content embedded within mixed text strings.
- 🔡 **Custom Filtering**: `STR_FILTERCHARS` allows precision control over which characters are retained.
- 🧼 **Sanitization**: `STR_SANITIZE` is highly useful for cleaning data pulled from web sources, forms, or APIs.
- 🏷 **Camel Case Validation**: `STR_HASCAP_AFTERFIRST` assists in detecting improperly formatted field names.
- 🔍 **Structural Parsing**: `STR_REMOVE_ENCLOSED` and `STR_TEXTBETWEEN` simplify extraction of substrings embedded within delimiters.
- 🔬 **Character-Level Arrays**: `STR_SPLITCHARS` and `STR_UNIQUECHARS` make downstream text analysis and visualization easy.

---

## ⚙️ Requirements

- ✅ Modern Excel with LAMBDA and dynamic array support (Office 365 or Excel 2021+).
- 🚫 No external dependencies or constant sets required.

---

## 📎 File Contents

- `String Excel LAMBDA Suite.txt`: Master definitions file with inline comments and annotated examples.
- `README.md`: This guide (suitable for GitHub or Obsidian publishing).
