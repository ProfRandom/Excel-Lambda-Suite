### `RECIP(input)`

Returns the **reciprocal** (multiplicative inverse) of a number.

#### Parameters:
- `input` *(required)* – A nonzero numeric value.

#### Returns:
- A single decimal value equal to `1 / input`.

#### Examples:
```excel
RECIP(4) → 0.25  
RECIP(0.2) → 5  
RECIP(-2) → -0.5  
```

#### Notes:
- Returns `#DIV/0!` if `input = 0`
- Useful for computing inverse rates, flipping fractions, or simplifying certain formulas (e.g., reciprocal time or frequency).

---
### `FRAC(input, [mode])`

Returns the **fractional part** of a number, with optional sign preservation.

#### Parameters:
- `input` *(required)* – The numeric value to evaluate.
- `mode` *(optional)* – Output mode (default = `0`):
  - `0`: Always returns the positive fractional part (e.g., `0.25`)
  - `1`: Returns the fractional part with its original sign (e.g., `-0.25`)

#### Returns:
- A decimal between `0` and `1` (or between `-1` and `0` if `mode = 1`)

#### Examples:
```excel
FRAC(3.75)       → 0.75
FRAC(-3.75)      → 0.75
FRAC(-3.75, 1)   → -0.75
```

#### Notes:
- Complements Excel’s `TRUNC` and `QUOTIENT` functions.
- Especially useful for isolating non-integer values or detecting offset from whole numbers.
- Signed mode (`1`) can distinguish whether a number is just below or just above an integer.

---
### `ROOT(n, [x])`

Returns the x-th root of a number. Defaults to square root if no degree is specified.

#### Parameters:
- `n` *(required)* – The number to take the root of.
- `x` *(optional)* – The root degree (default = `2` for square root).

#### Returns:
- A decimal number representing the x-th root of `n`.

#### Examples:
```excel
ROOT(16)        → 4
ROOT(27, 3)     → 3
ROOT(81, 0.5)   → 9
```

#### Notes:

- If `x` is omitted, the function returns the square root of `n`.    
- Returns a `#NUM!` error if `n` is negative (no support for complex roots).    
- Accepts fractional and non-integer root degrees (e.g., `1.5`, `0.5`, etc).    
- Will return a `#DIV/0!` error if `x = 0` (division by zero).    
- Use this function for general-purpose root operations beyond what Excel's `SQRT()` supports.

---
### `FORMTEXT(input, [mode])`

Extracts and formats the formula from a referenced cell, with several display modes.

#### Parameters:
- `input` *(required)* — A reference to a cell containing a formula.
- `mode` *(optional)* — Output mode:
  - `0`: Returns just the bare function name(s)
  - `1`: Returns cleaned assignment-style (e.g., `A1:=TEXTJOIN(...)`)
  - `2` *(default)*: Assignment-style using raw Excel formula (e.g., `A1:=TEXTJOIN(...)`)
  - `3`: Raw output from `FORMULATEXT`

#### Returns:
- A text string representing the formula in the selected format.

#### Examples:
```excel
FORMTEXT(A1, 0) → "TEXTJOIN"
FORMTEXT(A1, 1) → "A1:=TEXTJOIN(...)"
FORMTEXT(A1, 2) → "A1:=TEXTJOIN(CHAR(10), TRUE, A1:A5)"
FORMTEXT(A1, 3) → "=TEXTJOIN(CHAR(10), TRUE, A1:A5)"
```

#### Notes:

- Removes equal sign (`=`) for display formatting in modes 1 and 2.    
- Mode 0 can be used to extract only function names (e.g., for classification).    
- Mode 3 returns the raw Excel formula for debugging/logging.    
- Great for creating custom **formula audit dashboards**, or building **self-documenting templates**.

---
### `FORMULA_TEXT(cell)`

Returns a one-line, labeled version of the formula from a given cell, removing the leading equal sign and prepending the cell reference.

#### Parameters:

- `cell` _(required)_ — A reference to a cell containing a formula.
    
#### Returns:

- A text string like `"B3:= RECIP(ROOT(PI(),3))"` showing the formula content in an easy-to-read display format.
    
#### Example:
```excel
FORMULA_TEXT(B3)               → "B3:= RECIP(1.414)"
```
#### Notes:

- Ideal for audits, dashboards, printouts, and documenting named LAMBDA functions.    
- This function does not inspect, modify, or validate the formula—it simply extracts and formats it.    
- Equivalent to `CELL("address", ref) & ":= " & TEXTAFTER(FORMULATEXT(ref), "=")`.
---
### `ROUND_FIX(number, places, [as_text], [use_round])`

Rounds or truncates a number to a specified number of decimal places, with optional string output to ensure fixed-width formatting and trailing zero preservation.

#### Parameters:

- `number` _(required)_ — The numeric value to process.    
- `places` _(required)_ — Number of decimal places to retain.    
- `as_text` _(optional)_ — If `TRUE`, returns the result as a text string with trailing zeros. Defaults to `FALSE`.    
- `use_round` _(optional)_ — If `TRUE`, applies rounding. If omitted or `FALSE`, the number is truncated.
    

#### Returns:

- A numeric or text-formatted version of the number, rounded or truncated to the desired precision.
    
#### Examples:

```excel
ROUND_FIX(PI(), 2)                 → 3.14
ROUND_FIX(PI(), 3, TRUE)           → "3.141"
ROUND_FIX(PI(), 4, TRUE, FALSE)    → "3.1415"
ROUND_FIX(PI(), 12, FALSE)         → 3.141592654   // capped at 9 decimals
ROUND_FIX(PI(), 12, TRUE)          → "3.141592653590"
```

#### Notes:

- Excel’s numeric display is limited to ~9 decimal places. If `as_text` is `FALSE`, precision is capped to 9 to avoid display anomalies.    
- Use `as_text = TRUE` to show exact decimal formatting with trailing zeros preserved.    
- Useful for numeric display in reports, rounding constants, or formatting math outputs for consistent precision.