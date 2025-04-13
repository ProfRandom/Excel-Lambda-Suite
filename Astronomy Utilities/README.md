### `ASTRO_HAB_INDEX(orbital_dist, [nucleal_radius], [prec])`

Calculates a **normalized planetary habitability index** based on a planet’s orbital distance relative to a star’s **nucleal zone radius** (the center of its habitable zone).

#### Parameters:
- `orbital_dist` *(required)* – Planet’s orbital distance (in AU)
- `nucleal_radius` *(optional)* – Radius of the star’s nucleal zone (in AU); defaults to `1.0`
- `prec` *(optional)* – Decimal precision for rounding (default = `3`)

#### Returns:
- A numeric index value (e.g., `1.000`) if the planet is potentially habitable  
- `"U/I"` ("Uninhabitable/Invalid") if the planet is *too deep* inside the inner boundary of the habitable zone

#### Interpretation:
- `1.000` → Ideal alignment with the habitable zone
- `< 1.0` → Inside optimal band (possibly too hot)
- `> 1.0` → Outside optimal band (possibly too cold)
- `≤ 0` → `"U/I"` (Uninhabitable due to extreme proximity)

#### Examples:
```excel
ASTRO_HAB_INDEX(1.0)            → 1.000
ASTRO_HAB_INDEX(0.75, 1.0)      → 0.500
ASTRO_HAB_INDEX(2.5, 1.0)       → 1.628
ASTRO_HAB_INDEX(0.25, 1.0)      → "U/I"
```

#### Notes:

- The piecewise logic models habitability as a smooth curve across both sides of the habitable zone.    
- Can be adapted to different stellar types by changing the `nucleal_radius` input.    
- Use for planetary classification, biozone diagnostics, or worldbuilding logic.

---
### `ASTRO_SPECTRAL_DISTRIBUTION([type], [count], [precision])`

Returns a table showing the relative or scaled frequency distribution of stellar spectral classes (O, B, A, F, G, K, M).

#### Parameters:
- `type` *(optional)* — A spectral class to use as the baseline for scaling.
- `count` *(optional)* — The number of stars to scale against (default = 1).
- `precision` *(optional)* — Decimal precision for output (default = 3).

#### Returns:
A 2-column array:
- Column 1: Spectral class letter
- Column 2: Relative frequency (if `type` omitted) or scaled distribution (if `type` and `count` provided)

#### Examples:
```excel
ASTRO_SPECTRAL_DISTRIBUTION("G", 100)
→ {"O", 0; "B", 0.00125; "A", 0.00625; "F", 0.030303; "G", 0.076923; "K", 0.125; "M", 76.027}

ASTRO_SPECTRAL_DISTRIBUTION()
→ {"O", 0.0000003; "B", 0.00125; "A", 0.00625; "F", 0.030303; "G", 0.076923; "K", 0.125; "M", 0.760274}
```

#### Notes:

- If `type` is omitted or invalid, the result reflects relative abundance (based on 1/frequency).    
- If `type` is given, all other classes are scaled relative to its canonical frequency.  
- This can simulate synthetic stellar populations or support galactic structure models.

---
### `ASTRO_CALC_TEMP(subclass)`

Returns the effective temperature in Kelvin for a given stellar subclass (e.g. `"G7.3"`), using empirical high-temperature values and subclass span interpolation.

#### Parameters:

- `subclass` _(required)_ — A string representing the stellar classification, including optional decimal subclass fraction. Examples: `"F5"`, `"K2.6"`, `"M8.9"`.    

#### Returns:

- A numeric value representing the interpolated effective temperature in Kelvin.
    

#### Description:

This function uses a hardcoded matrix of spectral subclasses (O3–M9) with their corresponding high temperatures and temperature spans. The temperature for a fractional subclass (e.g., `"G7.3"`) is calculated via linear interpolation:

$$T = T_high - (fraction * span)$$
Where:

- `T_high` is the high temperature for the base subclass (e.g., `"G7"`)    
- `span` is the temperature difference to the next subclass    
- `fraction` is the decimal portion of the input (e.g., `.3`)
    
#### Examples:
```excel
ASTRO_CALC_TEMP("G7.3")   → 5529
ASTRO_CALC_TEMP("O4.4")   → 42300
ASTRO_CALC_TEMP("F8.45")  → 6121.5
ASTRO_CALC_TEMP("M8.6")   → 2456
```
#### Notes:

- Accepts and normalizes inputs with or without a decimal point.    
- Fractional interpolation is based on observed subclass transitions, not assumed linear scaling across spectral classes.    
- Designed for modeling, star classification, and parameter estimation in fictional or educational astrophysics simulations.
---
### `ASTRO_DISPLAY_SPECTRAL([type])`

Displays stellar subclass temperature and span data across the full main sequence spectral range (O3–M9). Can output either a full classification matrix or a focused table for a single spectral type.

#### Parameters:

- `type` _(optional)_ — A single-character string representing a major spectral class: `"O"`, `"B"`, `"A"`, `"F"`, `"G"`, `"K"`, or `"M"`. If omitted, the function returns the full spectral chart.
    
#### Returns:

- If no `type` is specified: A multi-column matrix displaying temperatures and spans for all subclasses (O3 through M9), grouped by spectral class.    
- If a specific `type` is provided: A two-column table listing subclass temperatures and spans for that spectral class only.
    
#### Description:

This function serves as a spectral classification reference tool. It returns either a broad overview of all 70 subclasses, or a filtered listing for a single spectral type. Each subclass entry includes:

- The effective temperature (`T_high`) at the upper end of the subclass range    
- The temperature span (K) between this subclass and the next
    
The full-table mode outputs a formatted matrix with class columns (O–M) and subclass indices (0–9). In type-specific mode, a simple vertical list is returned.

#### Examples:
```excel
ASTRO_DISPLAY_SPECTRAL()       → Full table view, O to M, 10 subclasses per type
ASTRO_DISPLAY_SPECTRAL("G")    → G0 to G9 temp & span ASTRO_DISPLAY_SPECTRAL("F")    → F0 to F9 temp & span
```
#### Notes:

- Internally uses hardcoded temperature and span data from real-world estimates.    
- Span represents the Kelvin drop between the current subclass and the next cooler one.    
- The function uses `VSTACK`, `HSTACK`, and `FILTER` logic to structure dynamic arrays.    
- Supersedes older utilities: `ASTRO_DISPLAY_BASE_DATA`, `_SEPARATED`, and `_BY_TYPE`.    
- Useful for visual reference, educational materials, or custom spectral interpolation logic.

---
### `ASTRO_STAR_ATTRIBUTES(mode, input, [precision])`

Calculates all major stellar parameters (temperature, mass, radius, luminosity, lifetime) from a single known value, using solar-relative scaling laws.

---

#### **Parameters:**

- `mode` _(required)_ — A string indicating which stellar attribute is being provided:  
    - `"K"` → Effective temperature (Kelvin)        
    - `"T"` → Normalized solar temperature (T / 5770)        
    - `"M"` → Mass in solar units        
    - `"R"` → Radius in solar units        
    - `"L"` → Luminosity in solar units        
    - `"V"` → Main-sequence lifetime in solar units        
- `input` _(required)_ — A numeric value for the input attribute corresponding to `mode`.    
- `precision` _(optional)_ — Number of decimal places to round each output. Default = `6`.
    

---

#### **Returns:**

A 2-column vertical table of stellar attributes:

- Labels: `"K"`, `"T"`, `"M"`, `"R"`, `"L"`, `"V"`
    
- Values: Corresponding calculations, with the input type marked by a ➔ arrow
    
#### **Scaling Formulas Used:**

Given normalized temperature `Tnorm` (i.e. `T = K / 5770` or derived):

- `K = T × 5770`    
- `M = T²`    
- `R = T^1.8`    
- `L = T^7.6`    
- `V = T⁻⁵`    
#### **Examples:**
```excel
`ASTRO_STAR_ATTRIBUTES("K", 5770)` → Returns all parameters for a solar-type star.
`ASTRO_STAR_ATTRIBUTES("M", 2.5, 3)` → Calculates K, T, R, L, V for a 2.5 M☉ star.
```

#### **Notes:**

- Automatically flags the input attribute with a ➔ in the output.    
- Based on generalized main-sequence stellar models.    
- Output is designed for comparison, modeling, and speculative use in educational or fictional astrophysics.    
- Values are **not** intended for high-precision physical simulation, but are consistent with common worldbuilding or pedagogical references.

---
