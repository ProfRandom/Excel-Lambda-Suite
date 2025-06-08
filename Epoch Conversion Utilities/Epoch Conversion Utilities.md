# EPOCH_ Utilities Suite

This suite contains high-precision Excel LAMBDA functions for converting between multiple year-based dating systems including Gregorian (AD/BC or CE/BCE), Holocene Era (HE), and "Before Present" (BP). Functions support both numeric and textual inputs, allow labeled or numeric output modes, and include optional fuzzy rounding for archaeological and historical estimation.

> See `epoch_utils.txt` for full function definitions, comments, and usage examples.

---

## 🧮 Function Index

| Function Name             | Description |
|--------------------------|-------------|
| `EPOCH_GREG_TO_HOLO`     | Converts a Gregorian year (signed number or string with BC/AD/CE/BCE) to Holocene Era (HE). |
| `EPOCH_HOLO_TO_GREG`     | Converts a Holocene Era year back into a Gregorian year (with optional labeled output). |
| `EPOCH_GREG_TO_BP`       | Converts a Gregorian year into a "Before Present" (BP) year, defaulting to labeled text output. |
| `EPOCH_BP_TO_GREG`       | Converts a BP year into a Gregorian date, optionally returning labeled output. |

---

## 📘 Usage Notes

- **Input Flexibility**: All functions support both signed numbers and string formats like `"753 BC"`, `"2024 CE"`, or `"44 AD"`.
- **Mode Switching**: Optional mode arguments control whether the output is raw numeric (`"NUM"`), labeled text (`"TXT"`), or includes fuzzy rounding (`"TXT;RND"`).
- **Fuzzy Rounding**: Archaeologically imprecise years (e.g., 21412 BP) can be rounded to nearest major magnitude (e.g., `"21000 BP"`).
- **Context-Aware Defaults**: Functions default to historically appropriate output conventions—e.g., `EPOCH_GREG_TO_BP` defaults to `"TXT;RND"` for academic readability.
- **Error Handling**: Functions return `#VALUE!` for malformed text strings or unsupported suffixes.

---

## 📂 Files

- `epoch_utils.txt`: Full suite with all function definitions, inline documentation, and examples.
