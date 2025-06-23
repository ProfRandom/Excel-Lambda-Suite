# ➗ Mathematics LAMBDA Suite for Excel

This suite provides Excel LAMBDA functions for general-purpose mathematical utilities, including rational approximations, divisor analysis, polygonal numbers, digital roots, and decimal manipulation. These tools extend Excel's native capabilities to support number theory, numeracy, and quantitative modeling.

---

## 📘 Overview

The suite includes tools for working with fractions, divisors, polygonal sequences, quadratic roots, decimal scaling, and digit-based calculations. These functions are useful in academic, simulation, educational, and analytical contexts where deeper mathematical manipulation is needed inside Excel.

---

## 📑 Function Index

| Function | Summary |
|---------|---------|
| `MATH_LCM_SCALED` | Computes scaled least common multiple (LCM) of two decimal values using precision scaling. |
| `MATH_LCM_SCALED_ARRAY` | Computes LCM across an array of decimal or fractional values with precision scaling. |
| `MATH_SPLIT_FRACTION` | Splits a fraction string (e.g. `"3/4"`) into its numerator and denominator as a 2-element array. |
| `MATH_FRACTION_TO_DECIMAL` | Converts a fraction string into a decimal value. |
| `MATH_SPLIT_INTEGER_DECIMAL` | Separates a number into its integer and fractional parts, returning both as an array. |
| `MATH_GET_DECIMAL_PART` | Extracts the decimal portion of a number, optionally signed. |
| `MATH_DIGITAL_ROOT` | Computes the digital root (iterative digit sum) of a number. |
| `MATH_DIGITAL_SUM` | Computes the simple (single-pass) sum of all digits of a number. |
| `MATH_POLYGONAL` | Returns the nth polygonal (figurate) number for any sided polygon (triangular, square, hexagonal, etc). |
| `MATH_QUADRATIC_REAL_ROOTS` | Calculates the real roots of a quadratic equation using the quadratic formula. |
| `MATH_NORMALIZE_DECIMAL` | Normalizes any number to a decimal < 1, preserving significant digits. |
| `MATH_APPROXIMATE_FRACTION` | Approximates a decimal as a fraction or mixed number string. |
| `MATH_LIST_DIVISORS` | Returns all positive integer divisors of a given number as an array or formatted string. |
| `MATH_METALLIC_MEAN` | Calculates the nth metallic mean (golden, silver, bronze, etc) with optional reciprocal. |
| `MATH_FORMAT_AS_FRACTION` | Converts a decimal to a simplified fraction string based on a fixed denominator base. |

---

## 🧩 Highlights and Tips

- 🧮 **Fractions Made Easy**: Use `MATH_APPROXIMATE_FRACTION` or `MATH_FORMAT_AS_FRACTION` to present decimal numbers as clean rational expressions.
- 🔢 **Divisors and Factors**: `MATH_LIST_DIVISORS` helps analyze number theory problems and factorization tasks.
- 🎯 **Polygonal Numbers**: `MATH_POLYGONAL` computes triangle, square, hexagonal, or higher-sided figurate numbers directly.
- 🧮 **Quadratic Solver**: `MATH_QUADRATIC_REAL_ROOTS` returns real solutions to quadratic equations, including formatted output modes.
- 🧱 **Decimal Splitting**: `MATH_SPLIT_INTEGER_DECIMAL` and `MATH_GET_DECIMAL_PART` allow you to separate integer and fractional parts with optional rounding.
- 🔢 **Digital Roots & Sums**: `MATH_DIGITAL_ROOT` and `MATH_DIGITAL_SUM` are useful for checksum analysis or numerology-style calculations.

---

## ⚙️ Requirements

- ✅ Modern Excel with LAMBDA and dynamic array support (Office 365 or Excel 2021+).
- 🚫 No external dependencies or constant sets required.

---

## 📎 File Contents

- `Mathematics Excel LAMBDA Suite.txt`: Master definitions file with inline comments and annotated examples.
- `README.md`: This guide (suitable for GitHub or Obsidian publishing).
