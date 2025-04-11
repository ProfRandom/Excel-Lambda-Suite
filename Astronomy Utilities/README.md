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
