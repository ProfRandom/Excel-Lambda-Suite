### `NUMNOTE_ENGINEERING(input, [prec])`

Formats a number into **engineering notation**, where the exponent is always a multiple of 3.

#### Parameters:
- `input` *(required)* — A numeric value
- `prec` *(optional)* — Number of decimal places to display (default = `2`)

#### Returns:
A string in the form of `"X.XXE+YY"`, suitable for scientific and engineering contexts.

#### Examples:
```excel
NUMNOTE_ENGINEERING(1234567)
→ "1.23E+06"

NUMNOTE_ENGINEERING(0.000478, 3)
→ "478.000E-06"
```

---
### `NUMNOTE_MAGNITUDE(input, [decprec])`

Converts a numeric value into a scaled string using metric-style engineering suffixes (e.g., `"k"`, `"M"`, `"G"`, etc.).

#### Parameters:
- `input` *(required)* — The numeric value to convert.
- `decprec` *(optional)* — Number of decimal places to display (default = `3`).

#### Returns:
A formatted string combining:
- The scaled numeric value
- An SI-style suffix (e.g., `"k"`, `"M"`, etc.)
- `"—"` if value is under 1000

#### Examples:
```excel
NUMNOTE_MAGNITUDE(123456)
→ "123.456 k"

NUMNOTE_MAGNITUDE(1000000000, 2)
→ "1.00 G"

NUMNOTE_MAGNITUDE(999)
→ "999.000 —"
```

#### Notes:

- Suffixes used: `"k"`, `"M"`, `"G"`, `"T"`, `"P"`, `"E"`, `"Z"`, `"Y"`, `"R"`, `"Q"`
    
- Maximum supported power: `10^30` (i.e., `"Q"`)
    
- Values below 1,000 return `"—"` as the suffix (e.g., `"999.000 —"`)
    
- Uses Excel’s `FIXED()` to preserve trailing zeros.
    
- Designed for dashboards, summaries, or display contexts needing compact notation.

---
### `NUMNOTE_POWERTAG(input, [mode])`

Generates a formatted exponent tag representing the order of magnitude of a given number — useful for labeling axes, formatting results, or annotating scientific notation.

#### Parameters:
- `input` *(required)* – A numeric value to analyze
- `mode` *(optional)* – Output format:
  - `0` (default): `"E+nn"` (e.g., `"E+03"`)
  - `1`: `"10^n"` (e.g., `"10^3"`)

#### Returns:
A string representing the base-10 power of the input value.

#### Examples:
```excel
NUMNOTE_POWERTAG(1000)
→ "E+03"

NUMNOTE_POWERTAG(0.0047, 1)
→ "10^-3"
```

#### Notes:

- This function returns **only** the exponent portion — not the coefficient.
    
- Uses `LOG10(...)` to determine magnitude.
    
- Values less than 1 will return a negative exponent (e.g., `0.01` → `"E-02"` or `"10^-2"`).
    
- If `mode` is invalid, the result is `"Invalid mode"` (instead of an Excel error).

---


