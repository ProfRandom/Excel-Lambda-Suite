# 📅 Epoch Conversion LAMBDA Suite for Excel

This suite offers Excel LAMBDA functions for converting between Gregorian calendar years (including BC/BCE notation) and Holocene Era (HE) / Myndhrean Calendar (MC) years. These tools are ideal for historical modeling, speculative worldbuilding, or working with extended timelines that cross conventional BCE/CE boundaries.

---

## 📘 Overview

Each function is designed to robustly handle both numeric and text inputs, parsing standard calendar notations while supporting signed year formats. Error handling is built-in for invalid or ambiguous inputs, and all conversions are fully self-contained for clean spreadsheet integration.

---

## 📑 Function Index

| Function | Summary |
|---------|---------|
| `EPOCH_GREG_TO_HOLO` | Converts Gregorian year (numeric or text format) to Holocene Era (HE). |
| `EPOCH_HOLO_TO_GREG` | Converts Holocene Era (HE) year into Gregorian year (signed integer). |

---

## 🧩 Highlights and Tips

- 🔢 **Flexible Input Parsing**: Accepts either signed numeric years (e.g., `-9600`) or text forms like `"753 BC"`, `"2024 CE"`, `"44 AD"`.
- 🌍 **Holocene Alignment**: Computes HE = Gregorian + 10,000, supporting continuous time scales that cross prehistoric boundaries.
- ❌ **Error Handling**: Invalid strings or malformed inputs produce clear Excel `#VALUE!` errors to flag issues.
- 🛠 **Bidirectional Support**: Both forward (`EPOCH_GREG_TO_HOLO`) and reverse (`EPOCH_HOLO_TO_GREG`) conversions are supported for full interchange.

---

## ⚙️ Requirements

- ✅ Modern Excel with LAMBDA and dynamic array support (Office 365 or Excel 2021+).
- 🚫 No external dependencies or constant sets required.

---

## 📎 File Contents

- `Epoch Conversion Excel LAMBDA Suite.txt`: Master definitions file with inline comments and annotated examples.
- `README.md`: This guide (suitable for GitHub or Obsidian publishing).
