# 🧠 Range Utilities Suite

A suite of Excel LAMBDA functions designed for advanced logical reasoning, pattern classification, and conditional handling across structured data, lists, and custom tests.

These functions operate beyond traditional TRUE/FALSE outputs—many return structural insights, diagnostic codes, or human-readable interpretations useful in workflows, validation chains, or classification tasks.

---
## Included Functions

### `RANGE_ANALYSIS(universal, check, [verbose])`

Analyzes and classifies the relationship between two ranges.

#### Possible Classifications:
- `"EQUAL"`: Sets are identical in both content and length.
- `"EQUIV"`: Sets are equal in size but share no items.
- `"PRSUB"`: The `check` range is a proper subset of `universal`.
- `"INTER"`: Sets share some values but are not equivalent or fully nested.
- `"FAILURE"`: Unable to classify — inputs are ambiguous or malformed.

#### Parameters:
- `universal` *(required)* – The reference set (U).
- `check` *(required)* – The set to compare (A).
- `verbose` *(optional)*:
  - `0` (default): returns symbolic tag only
  - `1`: returns descriptive sentence

#### Examples:
```excel
RANGE_ANALYSIS(A1:A10, B1:B5)
→ "PRSUB"

RANGE_ANALYSIS(A1:A10, B1:B5, 1)
→ "Proper subset: All elements from check found in universal."
```

#### Notes:
- Input ranges are automatically normalized with `TOCOL(..., 3)`.
- Duplicate values are accounted for.
- Use to drive conditional logic, audits, or data validation flows.
```
---

%% ### Coming Soon

- `ISIN` – Checks for presence of a value in a list (Boolean or index mode)
- `ONLYONE` – Returns TRUE only if exactly one condition is TRUE
- `ALLTRUE` / `ANYTRUE` – Array-based logical evaluators
- `SWITCHX` – Extended switch with fallback logic
- `IFX` – Logic-fluent if-statement interpreter for tiered expressions
 %%
---
### `RANGE_INTERSECT(universal, check, [sortMode], [showHeader])`

Returns a list of values that appear in both `universal` and `check` ranges — the intersection of two sets.

#### Parameters:
- `universal` *(required)* – The first range or list.
- `check` *(required)* – The second range to compare.
- `sortMode` *(optional)*:
  - `0` (default): preserve input order
  - `1`: sort alphabetically
- `showHeader` *(optional)*:
  - `TRUE` (default): includes symbolic header `"U ∩ A"`
  - `FALSE`: no header

#### Examples:
```excel
RANGE_INTERSECT(A1:A10, B1:B5)
→ {"U ∩ A"; value1; value2; ...}

RANGE_INTERSECT(A1:A10, B1:B5, 1, FALSE)
→ {sorted shared values}
```

#### Notes:
- All inputs are normalized via `TOCOL(..., 3)` to allow multi-column range support.
- Duplicate matches across ranges are removed.
- If there is no overlap, `"NONE"` is returned (with or without a header).
- For full two-way comparison, use `RANGE_ANALYSIS()` instead.

---
### `RANGE_COMPLEMENT(universal, check, [mode], [showHeader])`

Returns the **relative** or **absolute complement** between two ranges — that is, the values found in one but not the other.

#### Parameters:
- `universal` *(required)* – The complete set to compare from.
- `check` *(required)* – The set to compare against.
- `mode` *(optional)* – `"REL"` (default) or `"ABS"`:
  - `"REL"` → values in `universal` not in `check` (U \ A)
  - `"ABS"` → values in `check` not in `universal` (A \ U)
- `showHeader` *(optional)* – `TRUE` (default) or `FALSE` to display a symbolic header.

#### Examples:
```excel
RANGE_COMPLEMENT(A1:A10, B1:B5)
→ {"U \ A"; value1; value2; ...}

RANGE_COMPLEMENT(B1:B5, A1:A10, "ABS", FALSE)
→ {value1; value2; ...}
```

#### Notes:
- Inputs are automatically normalized to one-column arrays using `TOCOL(..., 3)` to handle full rectangular ranges.
- If no values are found, the function returns `"NONE"` (with or without a header).
- Use `SORT(...)` externally if needed — the header will remain at the top of the returned array.

#### Synonyms:
- Relative complement: U \\ A
- Absolute complement: A \\ U

---
### `RANGE_SYMDIFF(universal, check, [sortMode], [showHeader])`

Returns the **symmetric difference** between two ranges — that is, values found in either `universal` or `check`, but not in both.

#### Parameters:
- `universal` *(required)* – The first range to compare.
- `check` *(required)* – The second range to compare.
- `sortMode` *(optional)*:
  - `0` (default): preserve order
  - `1`: sort alphabetically
- `showHeader` *(optional)*:
  - `TRUE` (default): includes `"# U △ A"` label
  - `FALSE`: returns only the list

#### Examples:
```excel
RANGE_SYMDIFF(A1:A10, B1:B5)
→ {"# U △ A"; value1; value2; ...}

RANGE_SYMDIFF(A1:A10, B1:B5, 1, FALSE)
→ {sorted symmetric difference}
```

#### Notes:
- All inputs are normalized via `TOCOL(..., 3)` to allow full-range support.
- Duplicate values within inputs are retained if not found in the other set.
- If the two sets are identical, the result will be `"NONE"` (with or without header).


---
### `RANGE_UNION(universal, check, [sortMode], [showHeader])`

Returns the union of two lists or ranges — that is, all unique values found in either range.

#### Parameters:
- `universal` *(required)* – The first range to include.
- `check` *(required)* – The second range to include.
- `sortMode` *(optional)*:
  - `0` (default): preserve input order
  - `1`: sort alphabetically
- `showHeader` *(optional)*:
  - `FALSE` (default): no header
  - `TRUE`: adds `"U ∪ A"` label as first row

#### Examples:
```excel
RANGE_UNION(A1:A10, B1:B5)
→ {apple; banana; cherry; ...}

RANGE_UNION(A1:A10, B1:B5, 1, TRUE)
→ {"U ∪ A"; apple; banana; cherry; ...}
```

#### Notes:
- All inputs are normalized with `TOCOL(..., 3)` to ensure consistency.
- Duplicate values across ranges are automatically removed.
- Header (if shown) remains at top even when sorted.
- For a raw stacked list including duplicates, use `VSTACK(...)` directly.

---

### `RANGE_ISIN(universal, check, [mode])`

Checks whether one or more values from `check` exist in the `universal` range.

#### Parameters:
- `universal` *(required)* – The reference list or range to check against.
- `check` *(required)* – A value or array of values to test for membership.
- `mode` *(optional)* – Output format:
  - `0` (default): `TRUE`/`FALSE`
  - `1`: `"YES"`/`"NO"`
  - `2`: `1`/`0`
  - `3`: Two-column array `{check, result}` for verbose output

#### Examples:
```
RANGE_ISIN(A1:A10, "apple")
→ TRUE

RANGE_ISIN(A1:A10, {"apple", "pear"}, 1)
→ {"YES"; "NO"}

RANGE_ISIN(A1:A10, {"apple", "pear"}, 2)
→ {1; 0}

RANGE_ISIN(A1:A10, {"apple", "pear"}, 3)
→
{"apple", TRUE;
 "pear", FALSE}
```

#### Notes:
- All inputs are automatically flattened to one-column arrays using `TOCOL(..., 3)`.
- This ensures the function handles multi-row and multi-column ranges consistently.
- Ideal for conditional checking, dashboards, audit flags, or logical filtering.

---

#### Notes:
- Accepts both single values and arrays
- Matches behavior of `ISNUMBER(MATCH(...))` but more flexible
- Output is vertically aligned with the order of `check`
- Use `mode = 3` for a quick, standalone membership report

## Why This Exists

Standard Excel functions handle atomic logic (TRUE/FALSE) very well—but often fall short in **analyzing patterns across arrays**, **classifying structure**, or **making conditional logic readable at scale**.

This suite bridges that gap.
 
