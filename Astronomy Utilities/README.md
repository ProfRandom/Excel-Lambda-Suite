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

