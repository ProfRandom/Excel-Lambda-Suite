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
