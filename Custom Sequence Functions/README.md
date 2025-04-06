# Sequence Utility Functions

This module contains custom Excel LAMBDA functions that extend or emulate the behavior of the native `SEQUENCE()` function. Each function provides enhanced control over steps, repetition, boundary behavior, or interpolation.

All functions are lightweight, reusable, and compatible with Excel's dynamic array engine.

---

## 📦 Included Functions

### `SEQ_SPAN(lbound, ubound, count)`
Returns a fixed-length sequence of evenly spaced values between two bounds, including both endpoints.

- **Returns:** Horizontal array of `count` values  
- **Use case:** Evenly spaced interpolation across known endpoints

Example:
    =SEQ_SPAN(0, 10, 6)  // {0, 2, 4, 6, 8, 10}

---

### `SEQ_STEP(lbound, ubound, [step], [mode])`
Returns a dynamic-length sequence using a custom step size, ascending or descending.

- **Returns:** Horizontal or vertical array  
- **Parameters:**
  - `step` (default = 1)
  - `mode` (0 = row, 1 = column)  
- **Use case:** Generating sequences with arbitrary step size

Example:
    =SEQ_STEP(3, 11, 2)       // {3, 5, 7, 9, 11}  
    =SEQ_STEP(10, 0, -2, 1)   // vertical list from 10 down to 0

---

### `SEQ_BOUND(lbound, ubound, count, [mode], [rnd])`
Returns a sequence of evenly spaced values with optional control over bound inclusion.

- **Returns:** Horizontal array  
- **Modes:**
  - `0` = include both bounds (default)
  - `1` = exclude upper bound
  - `2` = exclude lower bound
  - `3` = exclude both bounds  
- **Use case:** Trimmed interpolation or midpoint generation

Example:
    =SEQ_BOUND(0, 1, 4, 0)  // {0.000, 0.250, 0.500, 0.750, 1.000}  
    =SEQ_BOUND(0, 1, 4, 3)  // {0.200, 0.400, 0.600}

---

### `SEQ_REPEAT(start, end, repeat, [repeatMode])`
Repeats either each value or the full sequence a specified number of times.

- **repeatMode:**
  - `0` = repeat each value
  - `1` = repeat entire sequence  
- **Returns:** Vertical array of repeated values

Example:
    =SEQ_REPEAT(1, 3, 2, 0)  // {1; 1; 2; 2; 3; 3}  
    =SEQ_REPEAT(1, 3, 2, 1)  // {1; 2; 3; 1; 2; 3}

---

## 🧪 Workbook Structure

Each function is defined and tested in its own tab:
- `SPAN`, `STEP`, `BOUND`, `REPEAT`

Each tab includes:
- Inline documentation
- Multiple usage examples
- Live outputs for quick verification

To use a function, open the workbook, copy the desired named LAMBDA definition from the Name Manager, and paste it into your target workbook.

---

## 💡 Author Notes

All functions are implemented using Excel’s native [LAMBDA](https://support.microsoft.com/en-us/office/lambda-function-bd212d27-1cd1-4321-a34a-ccbf254b8b67) framework. No VBA, macros, or external dependencies are required.

This repository is part of a modular Excel function suite intended to minimize clutter and maximize reusability. Each group of functions is organized by purpose (e.g., sequence generation, text utilities, date logic).

**License:** MIT (or update this section as desired)
