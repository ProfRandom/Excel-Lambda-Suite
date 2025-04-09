### `CONVERT_TEMP_C_TO_F(C, [precision])`

Converts a temperature from degrees Celsius to Fahrenheit.

#### Parameters:
- `C` *(required)* – A temperature in degrees Celsius
- `precision` *(optional)* – Number of decimal places to round to (default = `3`)

#### Returns:
- A numeric value in degrees Fahrenheit

#### Examples:
```excel
CONVERT_TEMP_C_TO_F(0) → 32
CONVERT_TEMP_C_TO_F(100, 2) → 212.00
CONVERT_TEMP_C_TO_F(-40) → -40.000
```

#### Notes:
- Negative values are supported.
- If `precision` is omitted or invalid (e.g., negative), it defaults to `3`.
- Uses the standard formula: **F = (C × 9/5) + 32**

---
### `CONVERT_TEMP_F_TO_C(F, [precision])`

Converts a temperature from degrees Fahrenheit to Celsius.

#### Parameters:
- `F` *(required)* – A temperature in degrees Fahrenheit
- `precision` *(optional)* – Number of decimal places to round to (default = `3`)

#### Returns:
- A numeric value in degrees Celsius

#### Examples:
```excel
CONVERT_TEMP_F_TO_C(32) → 0
CONVERT_TEMP_F_TO_C(212, 2) → 100.00
CONVERT_TEMP_F_TO_C(-40) → -40.000
```

#### Notes:
- Negative and fractional values are supported.
- If `precision` is omitted or invalid (e.g., negative), it defaults to `3`.
- Uses the standard formula: **C = (F − 32) × 5/9**

---
### `FORMAT_FEET_AND_INCHES(input, [style], [denom], [precision])`

Converts a decimal foot measurement into a formatted feet-and-inches string.

#### Parameters:
- `input` *(required)* — A decimal number representing feet (e.g., `6.4375`)
- `style` *(optional)* — Output format style:
  - `0` (default): decimal-inch format (e.g., `6' 5.25"`)
  - `1`: fractional-inch format (e.g., `6' 5-1/4"`)
- `denom` *(optional)* — Fraction denominator (e.g., `16` for sixteenths; default = `16`)
- `precision` *(optional)* — Number of decimal places for decimal inches (style `0` only, default = `3`)

#### Examples:
```excel
FORMAT_FEET_AND_INCHES(6.4375)
→ "6' 5.25""

FORMAT_FEET_AND_INCHES(6.4375, 1)
→ "6' 5-1/4""

FORMAT_FEET_AND_INCHES(6.4375, 0, , 4)
→ "6' 5.2500""
```

#### Notes:
- When `style = 1`, the decimal is converted to a fraction and **simplified** (e.g., `0.5` → `1/2`)
- When `style = 0`, the decimal portion of the inches is **rounded** to `precision` places.
- Useful for converting CAD data, woodshop measurements, or architectural output.

---
### `FORMAT_INCH_FRACTION(input, [denom])`

Formats a decimal inch value into a string with whole inches and a simplified fractional inch (e.g., `2-3/8"`).

#### Parameters:
- `input` *(required)* – A decimal number representing inches (e.g., `2.375`)
- `denom` *(optional)* – The rounding denominator (e.g., `16`, `32`, default = `32`)

#### Returns:
A string like:
- `"2-3/8\""` (for 2.375)
- `"5\""` (for whole numbers)

#### Examples:
```excel
FORMAT_INCH_FRACTION(2.375, 16)
→ "2-3/8\""

FORMAT_INCH_FRACTION(5)
→ "5\""
```

#### Notes:
- Fractional component is simplified to lowest terms.
- Omitted if remainder is zero.
- Always includes the inch symbol (`"`) and a dash between whole and fractional parts.
- Use for woodworking, design specs, or imperial reporting where decimal precision must be converted to common measurements.

---
