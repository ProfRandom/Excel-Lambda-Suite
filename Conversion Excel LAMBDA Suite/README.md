# 🧪 Conversion Excel LAMBDA Suite

This suite contains LAMBDA functions for converting between commonly used measurement systems. It includes utilities for working with temperature units and formatting length measurements in imperial feet-and-inches notation.

All functions follow Excel's LAMBDA convention and are suitable for spill-enabled environments.

---

## Included Functions

### ✅ `CONVERT_TEMP_C_TO_F`
**Converts a Celsius temperature to Fahrenheit.**

- **Input:** `C` (Celsius), optional `precision`
- **Returns:** Temperature in °F
- **Example:** `CONVERT_TEMP_C_TO_F(0)` → 32

---

### ✅ `CONVERT_TEMP_F_TO_C`
**Converts a Fahrenheit temperature to Celsius.**

- **Input:** `F` (Fahrenheit), optional `precision`
- **Returns:** Temperature in °C
- **Example:** `CONVERT_TEMP_F_TO_C(212, 2)` → 100.00

---

### ✅ `FORMAT_FEET_AND_INCHES`
**Converts a decimal feet value into formatted feet + inches.**

- **Input:** `input` (e.g. 6.4375), optional `style`, `denom`, `precision`
- **Returns:** Text like `"6' 5.25"` or `"6' 5-1/4""`
- **Example:** `FORMAT_FEET_AND_INCHES(6.4375, 1)` → `"6' 5-1/4""`

---

### ✅ `FORMAT_INCH_FRACTION`
**Converts a decimal inch value into formatted fractional inches.**

- **Input:** `input` (e.g. 2.375), optional `denom`
- **Returns:** Text like `"2-3/8"` or `"5""`
- **Example:** `FORMAT_INCH_FRACTION(2.375, 16)` → `"2-3/8""`

---

## Notes

- All functions default to reasonable precision or formatting if optional arguments are omitted.
- These utilities are especially useful in engineering, woodworking, and other measurement-sensitive fields.

---

**📁 File:** `Conversion Excel LAMBDA Suite.txt`  
**📦 Suite:** Conversion

