## 🧮 SUM Function Suite

This suite contains functions designed to perform common arithmetic summation tasks across intervals, ranges, and structured numeric patterns. These are especially useful in controlled calculations, spreadsheet modeling, and custom sequence generation where built-in Excel functions fall short.

### Included Functions

- **`SUM_RANGE`**  
  Calculates the sum of a numeric sequence using an optional lower/upper bound and increment. Automatically handles ascending and descending patterns.

- **`SUM_BETWEEN_BOUNDS`**  
  Returns the sum of all values in a stepped arithmetic sequence from a lower bound to an upper limit, without exceeding the upper bound.

- **`SUM_N_TERMS`**  
  Computes the sum of an arithmetic progression given the starting value, number of terms, and optional increment. Can also return the upper bound only.

- **`SUM_INTEGERS`**  
  Calculates the sum of all integers from 1 to `n`, or just the even or odd numbers within that range.

---

Each function uses closed-form formulas for performance, is parameter-flexible (via optional arguments), and includes modes for alternate return values where applicable.

**See also**:  
- [`DIGITAL_ROOT`](#) and [`DIGITAL_SUM`](#) in the **Digit Suite**, for digit-based summations and symbolic operations.

---
### `SUM_N_TERMS(lbound, length, [increment], [mode])`

Returns the sum of an arithmetic progression based on a defined starting value, number of terms, and optional step size.

#### Parameters:
- `lbound` *(required)* – Starting value of the sequence.
- `length` *(required)* – Number of terms to include.
- `increment` *(optional)* – Step between terms (default = 1).
- `mode` *(optional)* –  
  - `0` (default): return the total sum  
  - `1`: return only the upper bound of the series

#### Example:
```
SUM_N_TERMS(4, 15, 5) → 585
```
*(Sums 4 + 9 + 14 + ... + 74)*

#### Notes:
- Uses the closed-form arithmetic series formula:  
  \( \text{sum} = \frac{n}{2} \left(2a + (n - 1)d\right) \)
- Useful for modeling uniform intervals, spacing calculations, or evaluating ranges with known length and increment.

---
### `SUM_INTEGERS(input, [mode])`

Calculates the sum of natural numbers up to a given value, with optional modes for even or odd summation.

#### Parameters:
- `input` *(required)* – The upper limit of the summation range.
- `mode` *(optional)* –  
  - `0` (default): sum of all integers from 1 to `input`  
  - `1`: sum of all even integers ≤ `input`  
  - `2`: sum of all odd integers ≤ `input`

#### Examples:
```
SUM_INTEGERS(10)       → 55   // 1 + 2 + 3 + ... + 10  
SUM_INTEGERS(10, 1)    → 30   // 2 + 4 + 6 + 8 + 10  
SUM_INTEGERS(10, 2)    → 25   // 1 + 3 + 5 + 7 + 9
```

#### Notes:
- Uses closed-form summation formulas for performance.
- Designed for fast access to common numeric sums without iteration.
- Internally adjusts for odd/even boundaries to ensure correctness.

---
### `SUM_RANGE(lbound, [ubound], [increment])`

Calculates the sum of an arithmetic sequence, with flexible support for ascending, descending, and default 1-to-`n` cases.

#### Parameters:
- `lbound` *(required)* – Lower bound of the sequence. If `ubound` is omitted, this is treated as the upper bound and `1` is used as the lower.
- `ubound` *(optional)* – Upper bound of the sequence. If omitted, the function treats `lbound` as the upper bound instead.
- `increment` *(optional)* – Step between values (default = 1).

#### Examples:
```
SUM_RANGE(1, 10)       → 55    // 1 + 2 + ... + 10  
SUM_RANGE(3, 15, 3)    → 45    // 3 + 6 + 9 + 12 + 15  
SUM_RANGE(10)          → 55    // Same as SUM_RANGE(1, 10)
```

#### Notes:
- Uses the arithmetic series formula for performance:
  \[
  \text{sum} = \frac{n}{2} \left(2a + (n - 1)d\right)
  \]
- Gracefully handles reversed sequences, optional inputs, and non-unit steps.
- Can functionally replace `SUM_INTEGERS` when `increment = 1`.


---
### `SUM_BETWEEN_BOUNDS(lbound, [ubound], [increment])`

Returns the sum of all values in an arithmetic sequence that begins at `lbound` and steps by a fixed increment without exceeding `ubound`.

#### Parameters:
- `lbound` *(required)* – Starting value of the sequence.
- `ubound` *(optional)* – Upper limit; if omitted, returns `lbound` as a single-term sum.
- `increment` *(optional)* – Step between terms (default = 1).

#### Example:
```
SUM_BETWEEN_BOUNDS(4, 20, 3) → 69
// Sums: 4 + 7 + 10 + 13 + 16 + 19
```

#### Notes:
- Uses the closed-form arithmetic series formula—no iteration required.
- Only includes full steps that do **not exceed** the upper bound.
- Ideal for range-controlled summations with safe upper limits.

---
---

---

### 📊 Sample Workbook

For hands-on examples and live formula testing, see:

** [`Summing Utils.xlsx`](Summing%20Utils.xlsx) **
This file contains:
- Input/output demos for each function in the suite
- Sample scenarios with expected results
- Pre-loaded formulas for quick exploration

> Tip: Copy any function from this sheet into your own workbook to begin using it immediately.
